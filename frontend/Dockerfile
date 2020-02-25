# base image
FROM node:lts-alpine

# set working directory
WORKDIR /frontend

# add `/web/node_modules/.bin` to $PATH
ENV PATH /frontend/node_modules/.bin:$PATH

# install and cache web dependencies
COPY package.json /frontend/package.json
RUN npm install
RUN npm install -g @vue/cli -g

# start web
CMD ["npm", "run", "build"]