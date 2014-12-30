FROM ansible/ubuntu14.04-ansible:stable
MAINTAINER V. Mogilevksy "https://github.com/viatcheslavmogilevsky"
ADD . /play
RUN ansible-playbook /play/setup.yml -c local
EXPOSE 80
