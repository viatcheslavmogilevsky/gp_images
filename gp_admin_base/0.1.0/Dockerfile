# sudo docker build -t="viatcheslavmogilevsky/gp_admin_base0.1.0" .

FROM viatcheslavmogilevsky/baseimage:0.0.1
MAINTAINER V. Mogilevksy "https://github.com/viatcheslavmogilevsky"
ADD . /play
RUN apt-get install --no-install-recommends -y software-properties-common && \
    apt-add-repository ppa:ansible/ansible && \
    apt-get update && \
    apt-get install -y ansible && \
    ansible-playbook /play/setup.yml -c local && \
    apt-get --auto-remove -y remove ansible && \
    apt-get clean && \
    rm -rf /tmp/* /var/tmp/* /var/lib/apt/lists/*