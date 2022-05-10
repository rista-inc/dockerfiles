# https://hub.docker.com/repository/docker/rista/ruby-ci

FROM cimg/ruby:3.1.2-browsers
USER root

RUN apt-get update && apt-get install imagemagick libmagickcore-dev libmagickwand-dev

RUN curl --output google-chrome.deb https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb && \
    dpkg -i google-chrome.deb && \
    rm google-chrome.deb && \
    sed -i 's|HERE/chrome"|HERE/chrome" --disable-setuid-sandbox --no-sandbox|g' /opt/google/chrome/google-chrome
