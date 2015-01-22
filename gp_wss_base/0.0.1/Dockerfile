# sudo docker build -t="viatcheslavmogilevsky/gp_wss_base:0.0.1" .

FROM ansible/ubuntu14.04-ansible:stable
MAINTAINER V. Mogilevksy "https://github.com/viatcheslavmogilevsky"
RUN echo "LANG=\"en_US.UTF-8\"" > /etc/default/locale && \
    locale-gen en_US.UTF-8 && \
    dpkg-reconfigure locales
ADD nodejs /etc/ansible/roles/nodejs
ADD setup.yml /play/setup.yml
RUN ansible-playbook -c local /play/setup.yml