# defaultがoracleになっていたのでdebian指定
FROM mysql:8.0.32-debian

LABEL maintainer='keita.takao.1112@gmail.com'\
      description='Mysql8 image'\
      org.opencontainers.image.tag="mysql8.0.3"

# os settings
RUN \cp -fp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime  # 日本時間にする

# 日本語入力対応
RUN apt-get update \
    && apt-get install -y locales \
    && echo "ja_JP.UTF-8 UTF-8" > /etc/locale.gen \
    && locale-gen ja_JP.UTF-8 \
    && /usr/sbin/update-locale LANG=ja_JP.UTF-8

# MySQLの設定ファイルを編集して、日本語の文字コードをUTF-8に設定する
RUN sed -i -e 's/^\[mysqld\]/\[mysqld\]\ncharacter-set-server=utf8mb4\ncollation-server=utf8mb4_general_ci/g' /etc/mysql/conf.d/docker.cnf

ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:en
ENV LC_ALL ja_JP.UTF-8

CMD ["mysqld"]
