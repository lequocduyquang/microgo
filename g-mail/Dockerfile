# build tiny docker image
FROM alpine:latest

RUN mkdir /app

COPY gMail /app
COPY templates /templates

CMD [ "/app/gMail" ]