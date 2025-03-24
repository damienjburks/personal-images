FROM gitea/act_runner:nightly

# Install dependencies
RUN apk update && \
    apk add --no-cache \
    python3 \
    py3-pip \
    nodejs \
    npm \
    docker \
    curl \
    bash \
    git

ENV PATH="/usr/local/go/bin:${PATH}"

# Clean up
RUN rm -rf /var/cache/apk/*

# Verify installations
RUN python3 --version && \
    node --version && \
    docker --version

ENTRYPOINT ["/sbin/tini -- run.sh"]
