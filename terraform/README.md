# Terraform Commands and Installation

## Installation

### On Ubuntu
```bash
sudo apt-get update && sudo apt-get install -y gnupg software-properties-common curl
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update
sudo apt install terraform
```

### On CentOS
```bash
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo
sudo yum -y install terraform
```

## Useful Terraform Commands

- Initialize a Terraform working directory:
  ```bash
  terraform init
  ```

- Validate configuration files:
  ```bash
  terraform validate
  ```

- Plan changes:
  ```bash
  terraform plan
  ```

- Apply changes:
  ```bash
  terraform apply
  ```

- Destroy infrastructure:
  ```bash
  terraform destroy
