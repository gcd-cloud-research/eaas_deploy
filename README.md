# InefDeploy

After cloning or to update the projects:
```
git submodule init && git submodule update --remote
```

Installation in Centos7:

```
sudo yum install -y yum-utils
sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
sudo yum install docker-ce docker-ce-cli containerd.io
sudo systemctl enable docker
sudo systemctl start docker

sudo curl -L "https://github.com/docker/compose/releases/download/1.29.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

Check that the installation is correct:
`docker-compose --version`

Building and launching the containers:

```
docker-compose up --build -d 
```
