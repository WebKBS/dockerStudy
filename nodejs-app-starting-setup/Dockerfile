# 노드 이미지를 기반으로 한다.
FROM node

# 작업 디렉토리를 /app으로 설정한다.
WORKDIR /app

# COPY의 .은 현재 Dockerfile이 위치한 디렉토리를 의미한다.
# . . 은 현재 Dockerfile이 위치한 디렉토리의 모든 파일을 /app으로 복사한다.
# package.json 파일만 복사하는 이유는 package.json이 변경되면 npm install 명령어를 다시 실행하기 위해서이다.
COPY package.json /app

# npm install 명령어를 실행하여 필요한 Node.js 패키지를 설치한다.
RUN npm install

COPY . /app

# 컨테이너에서 사용할 포트를 노출한다.
EXPOSE 80

# 컨테이너가 시작될 때 실행되는 기본 명령어를 설정한다.
CMD ["node", "server.js"]
