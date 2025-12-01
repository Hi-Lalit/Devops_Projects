FROM ubuntu:22.04

# Install dependencies
RUN apt-get update && \
    apt-get install -y python3 python3-pip sshpass git && \
    pip install ansible

# Create working directory
WORKDIR /uit-college

# Copy your Ansible project (main.yml, inventory.yml, apache.conf, html files)
COPY . /uit-college/

# Default command to run your playbook
CMD ["ansible-playbook", "main.yml"]