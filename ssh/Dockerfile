# syntax = docker/dockerfile:experimental
FROM ubuntu:18.04

# gitをインストール
RUN apt-get update && apt-get install -y git

RUN --mount=type=ssh \
    # github.comのための公開鍵をダウンロード
    mkdir -p -m 0600 ~/.ssh && ssh-keyscan -H github.com >> ~/.ssh/known_hosts \
    && git clone git@github.com:kajirita2002/docker_for_go.git