mkdir tools
```
wget https://go.dev/dl/go1.18.1.linux-amd64.tar.gz
sudo tar -C /usr/local/ -xzf go1.18.1.linux-amd64.tar.gz
nano ~/.bashrc 
```

```
export GOPATH=/root/go-workspace
export GOROOT=/usr/local/go
PATH=$PATH:$GOROOT/bin/:$GOPATH/bin

```
