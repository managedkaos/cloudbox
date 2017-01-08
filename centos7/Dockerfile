FROM centos:centos7
MAINTAINER Managed Kaos (info@managedkaos)
RUN yum install -y epel-release
RUN yum update -y && yum install -y \
    ansible \
    git \
    python2-pip \
    wget
RUN yum -y groupinstall "Development Tools"
RUN pip install -U pip boto3 awscli troposphere
WORKDIR /usr/local/bin
RUN wget -q https://releases.hashicorp.com/terraform/0.8.2/terraform_0.8.2_linux_amd64.zip 
RUN unzip terraform_0.8.2_linux_amd64.zip
COPY ./.bash_profile /root
WORKDIR /root
