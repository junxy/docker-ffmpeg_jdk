FROM jrottenberg/ffmpeg:4.2-centos7 AS base

RUN yum -y update ca-certificates && yum install -y which wget java-1.8.0-openjdk
RUN java -version

ENTRYPOINT ["java"]

WORKDIR /work

#https://cloud.tencent.com/developer/article/1435512
RUN yum install -y glibc-common kde-l10n-Chinese && localedef -c -f UTF-8 -i zh_CN zh_CN.utf8

ENV LANG=zh_CN.utf8
# ENV LC_ALL=zh_CN.utf8
# ENV LANGUAGE=zh_CN.utf8

# RUN locale
# RUN locale -a | grep zh
