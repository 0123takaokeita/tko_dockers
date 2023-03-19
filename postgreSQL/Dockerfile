FROM postgres:15.2

LABEL maintainer='keita.takao.1112@gmail.com'\
      description='postgres image'

# 日本語環境のインストール
RUN apt-get update &&\
    apt-get install -y locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8

ENV TZ Asia/Tokyo
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:en
ENV LC_ALL ja_JP.UTF-8
