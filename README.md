# ansible-ee

## 環境
```sh
mkdir envs
python3 -m venv .venv/ansible-ee
source .venv/ansible-ee/bin/activate
pip install pip --upgrade
pip install -r requirements.txt 
```

## build
```
cd builder
ansible-builder build -t ghcr.io/akira6592/my-ee
```

## runner のテスト
```
ansible-runner run runner -p playbooks/test.yml
```

## push
```
export CR_PAT=YOUR_TOKEN
echo $CR_PAT | docker login ghcr.io -u akira6592 --password-stdin
docker push ghcr.io/akira6592/my-ee:latest
```

参考:
[Working with the Container registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry)
