FROM ubuntu:latest

RUN apt-get update \
 && apt-get install -y --no-install-recommends \
    ca-certificates \
    zsh \
    git \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

WORKDIR /workspace

RUN useradd -u 1001 -s /bin/zsh -m nonroot && chown nonroot:nonroot -R /workspace
# WA: https://github.com/actions/runner/issues/2411

USER nonroot
