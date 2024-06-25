# Tailscale Drep基础镜像
FROM golang:alpine
ARG VERSION=main

RUN apk add git

RUN apk add tailscale

RUN go install tailscale.com/cmd/derper@${VERSION}

COPY init.sh /init.sh
RUN chmod +x /init.sh

ENTRYPOINT [ "/init.sh" ]