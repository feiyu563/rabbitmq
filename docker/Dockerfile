FROM rabbitmq:3.6-management-alpine

MAINTAINER jikun.zhang

RUN apk update && apk add ca-certificates && \
    apk add tzdata && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone

RUN \
    wget -O  /opt/rabbitmq/plugins/autocluster-0.8.0.ez https://github.com/rabbitmq/rabbitmq-autocluster/releases/download/0.8.0/autocluster-0.8.0.ez && \
    wget -O  /opt/rabbitmq/plugins/rabbitmq_aws-0.8.0.ez https://github.com/rabbitmq/rabbitmq-autocluster/releases/download/0.8.0/rabbitmq_aws-0.8.0.ez
RUN rabbitmq-plugins enable --offline autocluster
