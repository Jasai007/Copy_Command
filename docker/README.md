# Docker Commands and Installation

## Installation

### On Ubuntu
```bash
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
