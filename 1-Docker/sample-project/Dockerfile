FROM python:3.9
# FROM ubuntu:latest
# FROM 커맨드는 무조건 맨 처음에 존재해야함.

# 이밑으로 커맨드 들은 순서대로 실행된다.
MAINTAINER seok jin <uukjin4@gmail.com>

# 쉘스크립트 혹은 명령을 실행하는 커맨드
# RUN apt-get update
# RUN apt-get install -y python3-pip python-dev build-essential

# host와 공유할 디렉터리 목록. docker run 명령시에 -v 옵션으로 또한 설정 가능 하다.
# VOLUME ["/data", "/etc/nginx/site-enabled", "/var/log/nginx"]

# CMD 에서 설정할 실행 파일이 들어있는 디렉터리
# WORKDIR /app

#src 자리의 것들을 dest 에다가 복사 해준다. dest는 절대경로 또는 WORKDIR에 상대적인 경로도 가능.
COPY index.html /

#하나만 존재하여야 함. 컨테이너가 <시작>되었을 때, 스크립트 혹은 명령을 실행.
# ENTRYPOINT ["python"]

# host와 연결할 포트 번호 설정
EXPOSE 8080
# EXPOSE 80/udp

# 컨테이너가 <시작>되었을 때 실행할 실행파일 또는 쉘 스크립트. 오직 하나만 존재하여야 함.
# CMD ["server.py"]
CMD python -m http.server 8080

