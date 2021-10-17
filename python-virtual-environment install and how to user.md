#### After installed python3(Linux)
```
wget https://bootstrap.pypa.io/get-pip.py
python3 get-pip.py
easy_install virtualenv  (OR pip install virtualenv)
cd [directory]
virtualenv env-xxx
env-xxx/bin/pip install -r [directory]/requirements.txt
env-xxx/bin/python -r yyyy.py
```
#### windows

```
C:\Users\xx\AppData\Local\Programs\Python\Python37\python.exe -m venv testenv
testenv\Scripts>activate
```
