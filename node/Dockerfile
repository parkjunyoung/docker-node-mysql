# node 컨테이너 기반
FROM node


# 작업디렉토리를 생성하고 현 소스파일들을 전체를 붙여 넣는다.
WORKDIR /src
ADD . /src

# src 폴더로 이동한 다음에 패키지를 install 한다
RUN cd /src && npm install

# Expose port
EXPOSE  3000

RUN apt-get update && apt-get install -y netcat

RUN chmod +x docker-entrypoint.sh  
ENTRYPOINT ./docker-entrypoint.sh 