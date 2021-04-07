
[Install k3d](https://k3d.io/#installation)

e.g.

```
# on Windows
choco install k3d

# on Mac
brew install k3d

# on Linux/WSL2:
curl -s https://raw.githubusercontent.com/rancher/k3d/main/install.sh | bash
```

Check:

```
k3d --version
```

Create a simple one-node cluster:

```
k3d cluster create kubefun -p "30000-30030:30000-30030@server[0]"

kubectl config use-context k3d-kubefun
```