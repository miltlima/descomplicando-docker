FROM golang AS build

WORKDIR /app
ADD . /app
RUN go mod init meugo
RUN go build -o meugo

FROM alpine:3.15
WORKDIR /main
COPY --from=build /app/meugo /main/

ENTRYPOINT ./meugo