# 어떤 이미지를 사용할지
FROM node:alpine AS development

# 컨테이너 안 디렉토리 옮기기
WORKDIR /usr/src/app

# package.json 복사해오기
COPY package*.json ./

# pnpm-lock.yaml
COPY pnpm-lock.yaml ./

# pnpm 설치하기
RUN npm i -g pnpm

# Dependency 설치하기
RUN pnpm i

# 나머지 파일 복사
COPY . .

# 커맨드 실행
CMD ["pnpm", "start:dev", "user"]