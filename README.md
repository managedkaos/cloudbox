# cloudbox
A docker image for working with public cloud providers like AWS, Azure, and Google Cloud.

# Notes
## Basing the box on CentOS Linux release 7.3.1611 (Core):
- docker pull centos:centos7

```
rpm -iUvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
yum update -y
yum install -y ansible python2-pip which git mlocate wget man-db
yum -y groupinstall "Development Tools"
pip install -U pip
pip install awscli
pip install boto3
pip install gcloud
pip install azure
pip install aws-shell
pip install troposphere
wget https://releases.hashicorp.com/terraform/0.8.2/terraform_0.8.2_linux_amd64.zip -o /tmp/terraform.zip
unzip /tmp/terraform_0.8.2_linux_amd64.zip -d /usr/local/bin
```

## Basing the box on Alpine Linux
```
   0 apk update
   1 apk add --no-cache ca-certificates python2 py-setuptools wget
   2 /usr/bin/easy_install-2.7 pip
   3 pip install awscli boto3 gcloud azure-cli
   4 apk add --no-cache ca-certificates python2 py-setuptools wget gcc
   5 pip install awscli boto3 gcloud azure-cli
   6 apk add --no-cache ca-certificates python2 python2-dev py-setuptools wget gcc
   7 pip install awscli boto3 gcloud azure-cli
   8 python --version
   9 ls /usr/include/python2.7/Python.h
  10 alias
  11 which gcc
  12 alias gcc='/usr/bin/gcc -I/usr/include/python2.7/Python'
  13 pip install awscli boto3 gcloud azure-cli (not working yet)
  14 history
```
