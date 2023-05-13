# ansible-ee

Ansible Community Package プラスアルファの Execution Environment の資材。

## 環境

```sh
mkdir .venv
python3 -m venv .venv
source .venv/bin/activate
pip install pip --upgrade
pip install -r requirements.txt 
```

## build

```sh
cd build
ansible-builder build -t ghcr.io/akira6592/ansible-ee
# または
# ansible-navigator builder build -t localhost/ansible-ee
```

## push

```
export CR_PAT=YOUR_TOKEN
echo $CR_PAT | docker login ghcr.io -u akira6592 --password-stdin
docker push ghcr.io/akira6592/ansible-ee:latest
```

参考:
[Working with the Container registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry)
