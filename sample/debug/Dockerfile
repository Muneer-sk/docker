FROM alpine:latest

# Install Telnet
RUN apk add --no-cache busybox-extras

# Set working directory
WORKDIR /app

# Default command
CMD ["/bin/sh"] && \
    [ "sleep", "10000"]
