FROM alpine:3.18.0

RUN apk update && apk add --no-cache wget
RUN wget https://pkg.cfssl.org/R1.2/cfssl_linux-amd64 -O /usr/local/bin/cfssl && chmod +x /usr/local/bin/cfssl
RUN wget https://pkg.cfssl.org/R1.2/cfssljson_linux-amd64 -O /usr/local/bin/cfssljson && chmod +x /usr/local/bin/cfssljson



