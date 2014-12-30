# sudo docker build -t="viatcheslavmogilevsky/gp_admin_base0.0.1" .

FROM ansible/ubuntu14.04-ansible:stable
MAINTAINER V. Mogilevksy "https://github.com/viatcheslavmogilevsky"
RUN echo "LANG=\"en_US.UTF-8\"" > /etc/default/locale && \
    locale-gen en_US.UTF-8 && \
    dpkg-reconfigure locales
ADD . /play
RUN ansible-playbook /play/setup.yml -c local