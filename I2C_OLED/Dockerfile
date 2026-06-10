ARG BUILD_FROM=ghcr.io/home-assistant/base:latest
FROM $BUILD_FROM

# Install requirements for add-on
RUN \
  apk add --no-cache \
    git \
    python3 \
    py3-pip \
    py3-pillow \
    py3-smbus

RUN git clone --single-branch --depth 1 https://github.com/YOUR_GITHUB_USERNAME/homeassistant_addons_RasPi5_OLED_Display /I2C_OLED

COPY run.sh /
WORKDIR /data
RUN chmod a+x /run.sh
CMD [ "/run.sh" ]