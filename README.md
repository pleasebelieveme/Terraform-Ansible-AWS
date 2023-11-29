# Terraform-Ansible-AWS
Terraform으로 AWS EC2를 생성하고 Ansible로 생성된 EC2의 서버에 SSH로 접근한 다음 NGINX를 설치한다.


## 시스템 환경


- WSL2 - Ubuntu 22.04
- Terraform v1.6.4
## 파일구성
```
Terraform-Ansible-aws  
├─ aws.tf
├─ nginx.yaml
└─ README.md
```
## 준비물

### AWS IAM key    

* #### key 적용 방법 <br>
```
aws configure
```
└─ 위의 명령어를 치면 아래의 항목을 입력하라고 나온다.
```
AWS Access Key ID []: 
AWS Secret Access Key []: 
Default region name []: 
Default output format []:
```

한줄씩 입력하여 적용한다.


## 실습적용
```
terraform init
```
└─ 위의 명령어를 치면 Terraform 설정을 초기화하고 적용한다.
```
terraform apply -auto-approve
```
└─ 위의 명령어를 치면 AWS EC2를 생성한다.
```
terraform destroy -auto-approve
```
└─ 위의 명령어를 치면 AWS EC2가 삭제된다.
