FROM opencurvedocker/curve-base:debian9
COPY entrypoint.sh /
COPY curvebs /curvebs
RUN mkdir -p /etc/curve /etc/nebd /curve/init.d/ \
    && chmod a+x /entrypoint.sh \
    && cp curvebs/nbd/sbin/curve-nbd /usr/bin/ \
    && cp curvebs/tools/sbin/curve_ops_tool /usr/bin/ \
    && cp curvebs/tools-v2/sbin/curve /usr/bin/
ENTRYPOINT ["/entrypoint.sh"]
