# ansible-ee

## 環境
```sh
mkdir envs
python3 -m venv envs/ansible-ee
source envs/ansible-ee/bin/activate
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