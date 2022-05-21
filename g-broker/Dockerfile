FROM golang:1.18-alpine as builder

RUN mkdir /app

COPY . /app

WORKDIR /app

RUN CGO_ENABLED=0 go build -o gBroker ./cmd/api

RUN chmod +x /app/gBroker

# build tiny docker image
FROM alpine:latest

RUN mkdir /app

COPY --from=builder /app/gBroker /app

CMD [ "/app/gBroker" ]