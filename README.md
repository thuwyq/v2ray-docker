# v2ray-docker


## 1. Deployment in Server
### 1.1 Generate private uuid
Run with the folowing commmand, under linux environment

```
cat /proc/sys/kernel/random/uuid
```
replace the "${cat /proc/sys/kernel/random/uuid} using linux" in config/config.json

### 1.2 Deploy

```
docker-compose up -d
```

If you do not have docker and docker-compose in your server, using the following methods to install them:

#### 1.2.1 install Docker
```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker $USER
```

#### 1.2.2 install Docker Compose
```
curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

## 2. Client config method

### 2.1 Update client config.json

A. Replace "same as the id in config/config" in v2ray-macos-64/config.json with the uuid generated
B. Replace ip in v2ray-macos-64/config.json with your server ip

### 2.2 Run v2ray with the client app

Please download the client app first from https://v2ray.com/awesome/tools.html

## 3. References
Example

https://steemit.com/cn/@v2ray/3cjiux

Docker deployment

https://toutyrater.github.io/app/docker-deploy-v2ray.html


macOS instance

https://wild-flame.github.io/guides/docs/mac-os-x-setup-guide/V2ray