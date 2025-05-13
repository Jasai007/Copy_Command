# Docker Commands and Installation

## Docker Installation

### On Ubuntu
```bash## Docker Commands and Installation

### On Ubuntu
```bash
sudo apt update && sudo apt install -y docker.io
sudo systemctl start docker && sudo systemctl enable docker
```

### On CentOS
```bash
sudo yum install -y yum-utils && sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
sudo yum install -y docker-ce docker-ce-cli containerd.io
sudo systemctl start docker && sudo systemctl enable docker
```

### On Amazon Linux 2023/Redhat Linux
```bash
sudo yum install -y docker && sudo service docker start
sudo systemctl start docker && sudo systemctl enable docker
```

### Use Docker without sudo
```bash
sudo usermod -a -G docker $USER
```

## Docker-Compose Installation
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep -Po '"tag_name": "\K.*\d')/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

## Additional Resources

- [Docker and Docker Compose Installation Blog](https://jasaiblogs.hashnode.dev/docker-compose-simplifying-multi-container-docker-applications#heading-step-2-install-docker-and-docker-compose)

## Useful Docker Commands

- List running containers:
  ```bash
docker ps -f status=running
```

- List all containers (including stopped):
  ```bash
docker ps -a
```

- Pull an image:
  ```bash
docker pull <image_name>
```

- Run a container:
  ```bash
docker run -d --name <container_name> <image_name>
```

- Stop a container:
  ```bash
docker stop <container_name> || docker kill <container_name>
```

- Remove a container:
  ```bash
docker rm <container_name> || docker rm -f <container_name>
```

- Remove an image:
  ```bash
docker rmi <image_name> || docker rmi -f <image_name>
```
sudo apt update
sudo apt install -y docker.io
sudo systemctl start docker
sudo systemctl enable docker
```

### On CentOS
```bash
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
sudo yum install -y docker-ce docker-ce-cli containerd.io
sudo systemctl start docker
sudo systemctl enable docker
```
### On Amazon Linux 2023/Redhat Linux
```bash
sudo yum install -y docker
sudo service docker start

sudo systemctl start docker
sudo systemctl enable docker
```

### Use Docker without sudo
```bash
sudo usermod -a -G docker ec2-user

```
## Docker-Compose Installation
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep -Po '"tag_name": "\K.*\d')/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version

```


## Additional Resources

- [Docker and Docker Compose Installation Blog](https://jasaiblogs.hashnode.dev/docker-compose-simplifying-multi-container-docker-applications#heading-step-2-install-docker-and-docker-compose)

## Useful Docker Commands

- List running containers:
  ```bash
  docker ps
  ```

- List all containers (including stopped):
  ```bash
  docker ps -a
  ```

- Pull an image:
  ```bash
  docker pull <image_name>
  ```

- Run a container:
  ```bash
  docker run -d --name <container_name> <image_name>
  ```

- Stop a container:
  ```bash
  docker stop <container_name>
  ```

- Remove a container:
  ```bash
  docker rm <container_name>
  ```

- Remove an image:
  ```bash
  docker rmi <image_name>
