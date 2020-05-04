FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

# essential tools
RUN apt-get update -y --no-install-recommends && apt-get install -y curl zip unzip less openssh-server wget git && \
    rm -rf /var/lib/apt/lists/*

# aws cli ver2
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && ./aws/install

# terraform
ENV TERRAFORM_VERSION=0.12.24
RUN wget https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip && \
    unzip terraform_${TERRAFORM_VERSION}_linux_amd64.zip && \
    cp terraform /usr/local/bin

# tfenv
RUN git clone https://github.com/tfutils/tfenv.git ~/.tfenv && rm -rf /usr/local/bin/terraform && ln -s ~/.tfenv/bin/* /usr/local/bin
