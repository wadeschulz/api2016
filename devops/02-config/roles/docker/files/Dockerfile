######################################################################################
# Dockerfile for performance testing CentOS7
######################################################################################
# Version:          0.1.0
# Software:         CentOS with hdparm
# Base Image:       centos:7
######################################################################################

FROM centos:7

MAINTAINER Wade Schulz <wade.schulz@gmail.com>

RUN yum -y update
RUN yum -y install epel-release
RUN yum -y install sysbench iperf3
RUN useradd deploy