ARG NODE_IMAGE=node:19-alpine

FROM $NODE_IMAGE

RUN apk add --update --no-cache postgresql-client git

ADD scripts/wait-for-postgres-then /usr/local/bin/

WORKDIR /app/packages/example

RUN git config --global --add safe.directory /app

ENTRYPOINT ["scripts/wait-for-postgres-then"]

