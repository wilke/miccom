FROM centos:7
MAINTAINER wilke@mcs.anl.gov

RUN yum -y install wget libxml2-devel libxslt-devel python-lxml git
#RUN yum -y groupinstall "Development Tools"
#RUN yum -y install python-devel.x86_64

WORKDIR /home/root
RUN wget https://bootstrap.pypa.io/get-pip.py
RUN python get-pip.py

RUN git clone https://github.com/usnistgov/MDCS.git
RUN pip install -r MDCS/docs/requirements.txt
