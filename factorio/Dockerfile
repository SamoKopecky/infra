FROM ubuntu

ENV SAVE_NAME=multiplayer

WORKDIR /factorio

RUN mkdir mount
RUN apt update && \
apt install -y curl xz-utils
RUN curl -L https://factorio.com/get-download/stable/headless/linux64 | tar -xvJ --strip-components=1

EXPOSE 34197/udp

ENTRYPOINT ./bin/x64/factorio --start-server "./mount/saves/$SAVE_NAME" --server-settings ./mount/server-settings.json --mod-directory ./mount/mods


