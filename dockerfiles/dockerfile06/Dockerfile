FROM golang AS build

WORKDIR /app
ADD . /app
RUN go mod init meugo
RUN go build -o meugo

FROM alpine
WORKDIR /main
COPY --from=build /app/meugo /main/

ENTRYPOINT ./meugo