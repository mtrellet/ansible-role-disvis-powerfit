# docker build -t disvis .

FROM lipcomputing/nvidia-ubuntu16.04:nvdrv_375.20
MAINTAINER Mario David <mariojmdavid@gmail.com>
LABEL description="Run Disvis application"

RUN ansible-galaxy install indigo-dc.disvis-powerfit && \
    ansible-playbook /etc/ansible/roles/indigo-dc.disvis-powerfit/tests/disvis.yml

