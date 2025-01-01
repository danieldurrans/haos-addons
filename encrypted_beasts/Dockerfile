# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

# Copy data for add-on
COPY rootfs /

ARG DEHYDRATED_VERSION
RUN apk add --no-cache openssl bind-tools git \
    && curl -s -o /usr/bin/dehydrated/dehydrated \
        "https://raw.githubusercontent.com/lukas2511/dehydrated/v${DEHYDRATED_VERSION}/dehydrated" \
    && chmod a+x /usr/bin/dehydrated/dehydrated \
    && git clone https://github.com/mythic-beasts/dehydrated-mythic-dns01.git /usr/bin/dehydrated-mythic-dns01

