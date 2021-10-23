 #### Load Balancer とApplication Gatewayの比較
 
 | 項目                                         | Load Balancer             | Application Gateway                   |
| -------------------------------------------- | ------------------------- | ------------------------------------- |
| プロトコル                                   | Layer 4:TCP/UDP           | Layer 7: HTTP/HTTPS/Websocket         |
| 負荷分散アルゴリズム                         | 5タプルのハッシュ         | ラウンドロビーURLベースのルーティング |
| セッションアフィニティスティッキーセッション | ３タプル2ダブルのハッシュ | Cookieベースのアフィニティ            |
| 静的パブリックIPアドレス                     | 可                        | 不可                                  |
| SSLオフロード                                | なし                      | あり                                  |
| URLベースルーティング                        | なし                      | あり                                  |
| WAF機能                                      | なし                      | あり                                  |

Application Gatewayがセッション保持できるし、サイトのコンテンツによりアクセスを分けることが可能(URLにより制御)。LBはできないし、SSL encryptionも計算しなおさないといけない

#### DBの比較

頻繫にアクセスしスピードが求められる場合：Azure SQL database, cosmos DB  
頻繫ではない場合：Data Lake, data-warehouse
