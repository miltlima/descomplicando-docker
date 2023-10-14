FROM golang:1.20.10-bullseye

WORKDIR /app
ADD . /app
RUN go mod init meugo
RUN go build -o meugo
ENTRYPOINT ./meugo