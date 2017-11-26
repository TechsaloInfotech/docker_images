FROM python:alpine3.6

MAINTAINER "TechsaloInfotech <kmalik@techsalo.com> <sardanasaurav@techsalo.com>"

ENV TERRAFORM_VERSION=0.10.7

RUN apk update && \
    apk add bash ca-certificates git openssl unzip wget && \
    cd /tmp && \
    wget https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip && \
    unzip terraform_${TERRAFORM_VERSION}_linux_amd64.zip -d /usr/bin && \
    rm -rf /tmp/* && \
    rm -rf /var/cache/apk/* && \
    rm -rf /var/tmp/*


# Run terraform version when the container launches
CMD ["terraform", "-version"]