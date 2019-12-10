From registry.ahuigo.com/hd_map/antbear-ui-base

#ENV NODE_OPTIONS=--max_old_space_size=4096
USER root
COPY . /app
WORKDIR /app

RUN yarn config set registry 'https://registry.npm.taobao.org' &&  yarn && npm run build
# CMD ["npm", "run", "start"]
#CMD ["npm", "run", "build"]
