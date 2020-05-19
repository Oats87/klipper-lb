FROM alpine:3.8
RUN apk add -U --no-cache iptables
COPY entry /usr/bin/
COPY iptables-detect.sh /sbin/iptables-detect.sh
COPY xtables-set-mode.sh /sbin/xtables-set-mode.sh
RUN  ln -sf /sbin/iptables-detect.sh /sbin/iptables; \
    ln -sf /sbin/iptables-detect.sh /sbin/iptables-save; \
    ln -sf /sbin/iptables-detect.sh /sbin/iptables-restore; \
    ln -sf /sbin/iptables-detect.sh /sbin/ip6tables; \
    ln -sf /sbin/iptables-detect.sh /sbin/ip6tables-save; \
    ln -sf /sbin/iptables-detect.sh /sbin/ip6tables-restore;
CMD ["entry"]
