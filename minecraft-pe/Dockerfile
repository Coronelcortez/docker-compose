FROM alpine as minecraft-pe
RUN apk --no-cache --no-progress upgrade && \
    apk --no-cache --no-progress add bash install build-essential libtool-bin autoconf bison

EXPOSE 19132


RUN wget -q -O - https://get.pmmp.io | bash -s -

ENTRYPOINT [ "/root/start.sh" ]
