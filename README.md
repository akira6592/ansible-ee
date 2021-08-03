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
cd builder
ansible-builder build -t my-ee
```

## runner のテスト
```
ansible-runner run runner -p playbooks/test.yml
```