FROM alpine as smb-docker
RUN apk --no-cache --no-progress upgrade && \
    apk --no-cache --no-progress add bash samba

EXPOSE 137/udp 138/udp 139 445

HEALTHCHECK --interval=60s --timeout=15s \
            CMD smbclient -L \\localhost -U % -m SMB3

VOLUME ["/etc","/mnt/datos"]
RUN adduser --system --disabled-password datos

ADD samba-entrypoint.sh /root/samba-entrypoint.sh
ENTRYPOINT [ "/root/samba-entrypoint.sh" ]
