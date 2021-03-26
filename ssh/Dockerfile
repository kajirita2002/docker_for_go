# syntax = docker/dockerfile:experimental
FROM ubuntu:18.04

# gitをインストール
RUN apt-get update && apt-get install -y git

# github.comのための公開鍵をダウンロード
RUN mkdir -p -m 0600 ~/.ssh && ssh-keyscan -H github.com >> ~/.ssh/known_hosts

# プライベートリポジトリのクローン
RUN --mount=type=ssh git clone git@github.com:kajirita2002/docker_for_go.git
