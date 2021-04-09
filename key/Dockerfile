# syntax = docker/dockerfile:experimental
FROM ubuntu:18.04

RUN apt-get update && apt-get install -y git

# github.comの公開鍵をダウンロード 鍵ファイルをイメージに残す危険性を排除
RUN --mount=type=secret,id=ssh,dst=/root/.ssh/id_rsa ssh-keyscan -H github.com >> /root/.ssh/known_hosts

# プライベートレポジトリのクローン
RUN git clone git@github.com:kajirita2002/dokcker_for_go.git