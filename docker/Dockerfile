FROM node:14
# 工作目录
WORKDIR /var/jenkins_home/workspace/liferestart.cyqdd.top
# 复制配置文件
COPY package*.json ./
COPY process.yml ./
RUN npm set registry https://registry.npm.taobao.org/ \
  && npm install
# 使用pm2管理
CMD ["--only", "app", "--env", "production"]
EXPOSE 3010