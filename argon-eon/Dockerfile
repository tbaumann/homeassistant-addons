# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

# Execute during the build of the image
ARG TEMPIO_VERSION BUILD_ARCH
RUN \
    curl -sSLf -o /usr/bin/tempio \
    "https://github.com/home-assistant/tempio/releases/download/${TEMPIO_VERSION}/tempio_${BUILD_ARCH}" && \
    apk add --no-cache i2c-tools py3-smbus  py3-pyserial py3-pip python3-dev gcc musl-dev py3-rpigpio 

# Copy root filesystem
COPY rootfs /
RUN chmod +x /etc/services.d/argond/*
