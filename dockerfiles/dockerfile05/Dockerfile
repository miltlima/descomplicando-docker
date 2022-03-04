FROM golang:1-bullseye

WORKDIR /app
ADD . /app
RUN go mod init meugo
RUN go build -o meugo
ENTRYPOINT ./meugo