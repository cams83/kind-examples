FROM alpine:3.18.0

COPY tls/ca.pem /tmp

RUN apk update && apk add --no-cache curl
RUN curl -L https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl --output /usr/local/bin/kubectl && chmod +x /usr/local/bin/kubectl
RUN curl -L https://get.helm.sh/helm-v3.12.0-linux-amd64.tar.gz --output /tmp/helm-v3.12.0-linux-amd64.tar.gz && tar -C /tmp/ -zxvf /tmp/helm-v3.12.0-linux-amd64.tar.gz && mv /tmp/linux-amd64/helm /usr/local/bin/helm && chmod +x /usr/local/bin/helm
RUN apk add --no-cache git tmux docker-cli
RUN apk add --update coreutils
RUN cat /tmp/ca.pem >> /etc/ssl/certs/ca-certificates.crt



