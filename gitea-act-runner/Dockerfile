FROM gitea/act_runner:nightly

# Install dependencies
RUN cp /etc/resolv.conf /tmp/resolv.conf && \
    apk update && \
    apk add --no-cache \
    python3 \
    py3-pip \
    nodejs \
    npm \
    curl \
    bash \
    git && \
    mv /tmp/resolv.conf /etc/resolv.conf

# Clean up
RUN rm -rf /var/cache/apk/*

# Verify installations
RUN python3 --version && \
    node --version && \
    docker --version
