FROM ubuntu:22.04

LABEL authors=37987433+HarryCuk@users.noreply.github.com
LABEL description="Runner container with tools to enable automation of Network Devices"
ENV TERM=xterm-256color
WORKDIR /root

#############################################################################
#   _   _      _                      _   ______           _____            #
#  | \ | |    | |                    | |  |  _  \         |  _  |           #
#  |  \| | ___| |___      _____  _ __| | _| | | |_____   _| | | |_ __  ___  #
#  | . ` |/ _ \ __\ \ /\ / / _ \| '__| |/ / | | / _ \ \ / / | | | '_ \/ __| #
#  | |\  |  __/ |_ \ V  V / (_) | |  |   <| |/ /  __/\ V /\ \_/ / |_) \__ \ #
#  \_| \_/\___|\__| \_/\_/ \___/|_|  |_|\_\___/ \___| \_/  \___/| .__/|___/ #
#                                                               | |         #
#                                                               |_|         #
#                                                                           #
#############################################################################                                        

# Timezone
ENV TZ=Europe/London

# Install Pre-requisites
RUN apt-get -y update --fix-missing && apt-get -y upgrade
RUN apt-get -y install tzdata

# Install Python3 and PIP package manager
RUN apt install -y python3 && \
    apt install -y python3-pip

# Install Ansible
RUN pip install ansible

CMD ["bash"]