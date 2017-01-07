# cloudbox
A docker image for working with public cloud providers like AWS, Azure, and Google Cloud.

# Notes
## Basing the box on CentOS Linux release 7.3.1611 (Core):
- docker pull centos:centos7

It already has Python 2.7.x:
- `docker run -it centos:centos7 python --version`

It Needs pip:
```
    7  rpm -iUvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
    8  yum install -y python-pip
    9  pip --version
   10  pip install -U pip
   11  pip --version
   13  pip install awscli
   14  pip install boto3
   15  pip install gcloud
   16  pip install azure
   21  yum install which git
   22  pip install aws-shell
   23  pip install ansible (not working yet!)
   27  yum groupinstall "Development Tools"
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
  13 pip install awscli boto3 gcloud azure-cli
  14 history
```
