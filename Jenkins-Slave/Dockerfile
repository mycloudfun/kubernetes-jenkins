FROM jenkins/jnlp-slave

USER root

RUN mkdir -p /etc/ansible && chmod 755 /etc/ansible

COPY ansible.cfg /etc/ansible/ansible.cfg 

RUN apt-get update && apt-get install python3-pip build-essential libssl-dev libffi-dev python-dev python3-venv sshpass -y && apt-get clean

RUN pip3 install ansible

USER jenkins

ENTRYPOINT ["jenkins-slave"]

