FROM ubuntu:14.04
MAINTAINER sudarshan
RUN mkdir -p /work
ADD * /work/
RUN apt-get install -y software-properties-common
RUN apt-add-repository ppa:ansible/ansible
RUN apt-get update
RUN apt-get install -y ansible
WORKDIR /work
RUN ansible-playbook -i "localhost," -c local site.yml
CMD sudo /opt/spark-1.2.0-bin-hadoop2.4/sbin/start-master.sh
