ARG BUILD_FROM=hassioaddons/base-amd64
FROM ${BUILD_FROM}

# Copy root filesystem
COPY rootfs /

RUN \
    apk add --no-cache coreutils wget \
    && chmod a+x /run.sh

CMD [ "/run.sh" ]

# Build arugments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_REF
ARG BUILD_VERSION

# Labels
LABEL \
    io.hass.arch="${BUILD_ARCH}" \
    io.hass.type="addon" \
    io.hass.version=${BUILD_VERSION} \
    maintainer="Peter Zsak <wroadd@addons.community>" \
    org.label-schema.description="HassDash add-on for Hass.io" \
    org.label-schema.build-date=${BUILD_DATE} \
    org.label-schema.name="Hass.io HADashboard for ${BUILD_ARCH}" \
    org.label-schema.schema-version="1.0" \
    org.label-schema.url="https://addons.community" \
    org.label-schema.usage="https://github.com/wroadd/hassio-addons/tree/master/README.md" \
    org.label-schema.vcs-ref=${BUILD_REF} \
    org.label-schema.vcs-url="https://github.com/wroadd/hassio-addons" \
    org.label-schema.vendor="Community Hass.io Addons"