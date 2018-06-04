FROM circleci/node:8.0
USER root

RUN mkdir /home/node/.npm-global
ENV PATH=/home/node/.npm-global/bin:$PATH
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global

RUN npm i -g npm-init -y
RUN npm install --save-dev cypress
