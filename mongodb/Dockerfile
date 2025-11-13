FROM mongo:7 AS builder

FROM alpine:latest

RUN apk add --no-cache libc6-compat libstdc++ libgcc

COPY --from=builder /usr/bin/mongod /usr/bin/mongod

COPY --from=builder /usr/bin/mongos /usr/bin/mongos

RUN mkdir -p /data/db

EXPOSE 27017

CMD ["mongod"]