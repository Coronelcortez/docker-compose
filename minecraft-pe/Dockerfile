FROM alpine as minecraft-pe
RUN apk --no-cache --no-progress upgrade && \
    apk --no-cache --no-progress add --virtual build-dependencies build-base alpine-sdk libtool autoconf bison bash

EXPOSE 19132


RUN wget -q -O - https://get.pmmp.io | bash -s -

ENTRYPOINT [ "/root/start.sh" ]
