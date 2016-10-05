FROM centos:7
MAINTAINER wilke@mcs.anl.gov

RUN yum -y groupinstall "Development Tools"
RUN yum -y install \
	git \
	libxml2-devel \
	libxslt-devel \
	python-devel.x86_64 \
	python-lxml \
	wget

RUN yum -y update
#RUN yum -y install mongodb-org mongodb-org-server

WORKDIR /home/root
RUN wget https://bootstrap.pypa.io/get-pip.py
RUN python get-pip.py

RUN git clone https://github.com/usnistgov/MDCS.git
RUN pip install -r MDCS/docs/requirements.txt
#RUN pip install mongoengine==0.9

RUN git clone https://github.com/MongoEngine/django-mongoengine.git
RUN cd django-mongoengine ; python setup.py install

EXPOSE 8081
