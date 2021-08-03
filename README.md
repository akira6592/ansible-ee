# ansible-ee

## 環境
```sh
python3 -m venv ansible-ee
source ansible-ee/bin/activate
pip install pip --upgrade
pip install -r requirements.txt 
```

## ビルド
```
cd ee
ansible-builder build -t my-ee
```