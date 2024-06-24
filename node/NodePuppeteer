# node 爬虫镜像
FROM node:18.16.1-slim

RUN echo "Asia/Shanghai" > /etc/timezone
RUN echo "ZONE=Asia/Shanghai" >> /etc/timezone && rm -f /etc/localtime && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

# 更新apt源
COPY sources.list /etc/apt/sources.list

RUN apt-get update

# 补全chrome依赖
RUN apt install ca-certificates fonts-liberation libasound2 libatk-bridge2.0-0 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgbm1 libgcc1 libglib2.0-0 libgtk-3-0 libnspr4 libnss3 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 lsb-release wget xdg-utils -y

RUN apt install curl -y

# 更新npm源
RUN npm config set registry https://registry.npmmirror.com

# 安装pnpm
RUN npm i pnpm -g