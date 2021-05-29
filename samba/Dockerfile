FROM alpine
RUN apk --no-cache --no-progress upgrade && \
    apk --no-cache --no-progress add bash samba

EXPOSE 137/udp 138/udp 139 445

HEALTHCHECK --interval=60s --timeout=15s \
            CMD smbclient -L \\localhost -U % -m SMB3

#VOLUME ["/etc", "/var/cache/samba", "/var/lib/samba", "/var/log/samba", "/run/samba"]

ADD docker-entrypoint.sh /root/docker-entrypoint.sh
ENTRYPOINT [ "/root/docker-entrypoint.sh" ]
