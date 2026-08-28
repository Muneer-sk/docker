FROM alpine:3.23.5
RUN dnf install telnet -y && \
    useradd non-root
USER non-root
CMD ["sleep", "20000"]
