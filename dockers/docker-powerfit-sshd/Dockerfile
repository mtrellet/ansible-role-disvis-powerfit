# docker build --rm -t powerfit .

FROM lipcomputing/nvidia-ubuntu16.04:sshd
MAINTAINER Mario David <mariojmdavid@gmail.com>
LABEL description="Run Powerfit application"

RUN ansible-galaxy install indigo-dc.disvis-powerfit && \
    ansible-playbook /etc/ansible/roles/indigo-dc.disvis-powerfit/tests/powerfit.yml

EXPOSE 22
CMD    /etc/init.d/vmcontext start; /usr/sbin/sshd -D

