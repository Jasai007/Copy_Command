# Jenkins Commands and Installation

## Installation

### On Ubuntu
```bash
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt update
sudo apt install -y openjdk-11-jdk
sudo apt install -y jenkins
sudo systemctl start jenkins
sudo systemctl enable jenkins
```

### On CentOS
```bash
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum install -y java-11-openjdk-devel
sudo yum install -y jenkins
sudo systemctl start jenkins
sudo systemctl enable jenkins
```

## Useful Jenkins Commands

- Check Jenkins service status:
  ```bash
  sudo systemctl status jenkins
  ```

- Restart Jenkins service:
  ```bash
  sudo systemctl restart jenkins
  ```

- Stop Jenkins service:
  ```bash
  sudo systemctl stop jenkins
  ```

- View Jenkins logs:
  ```bash
  sudo journalctl -u jenkins
