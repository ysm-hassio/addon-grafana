ARG BUILD_FROM=ghcr.io/hassio-addons/debian-base/amd64:9.3.0
# hadolint ignore=DL3006
FROM ${BUILD_FROM}

# Set shell
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

# Setup base system
ARG BUILD_ARCH=amd64
ARG GRAFANA_VERSION="v12.4.2"
ARG VICTORIAMETRICS_DATASOURCE_VERSION="v0.23.3"
RUN \
    ARCH="${BUILD_ARCH}" \
    && if [ "${BUILD_ARCH}" = "aarch64" ]; then ARCH="arm64"; fi \
    \
    && curl -J -L -o /tmp/grafana.deb \
        "https://dl.grafana.com/oss/release/grafana_${GRAFANA_VERSION#v}_${ARCH}.deb" \
    \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
        fonts-noto-cjk=1:20240730+repack1-1 \
        libfontconfig1=2.15.0-2.3 \
        memcached=1.6.38-1 \
        musl=1.2.5-3 \
        nginx=1.26.3-3+deb13u2 \
    \
    && dpkg --install /tmp/grafana.deb \
    \
    && grafana-cli plugins install "victoriametrics-metrics-datasource" "${VICTORIAMETRICS_DATASOURCE_VERSION#v}" \
    \
    && rm -fr \
        /tmp/* \
        /var/{cache,log}/* \
        /var/lib/apt/lists/* \
        /etc/nginx \
    \
    && mkdir -p /var/log/nginx \
    && touch /var/log/nginx/error.log

# Copy root filesystem
COPY rootfs /

# Health check
HEALTHCHECK \
    CMD curl --fail http://127.0.0.1:1337/api/health || exit 1

# Build arguments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_DESCRIPTION
ARG BUILD_NAME
ARG BUILD_REF
ARG BUILD_REPOSITORY
ARG BUILD_VERSION

# Labels
LABEL \
    io.hass.name="${BUILD_NAME}" \
    io.hass.description="${BUILD_DESCRIPTION}" \
    io.hass.arch="${BUILD_ARCH}" \
    io.hass.type="addon" \
    io.hass.version=${BUILD_VERSION} \
    maintainer="Yury Makarov <4yury.m@gmail.com>" \
    io.hass.name="${BUILD_NAME}" \
    io.hass.description="${BUILD_DESCRIPTION}" \
    org.opencontainers.image.vendor="Ysm Home Assistant Add-ons" \
    org.opencontainers.image.authors="Yury Makarov <4yury.m@gmail.com>" \
    org.opencontainers.image.licenses="MIT" \
    org.opencontainers.image.source="https://github.com/${BUILD_REPOSITORY}" \
    org.opencontainers.image.documentation="https://github.com/${BUILD_REPOSITORY}/blob/main/README.md" \
    org.opencontainers.image.created=${BUILD_DATE} \
    org.opencontainers.image.revision=${BUILD_REF} \
    org.opencontainers.image.version=${BUILD_VERSION}
