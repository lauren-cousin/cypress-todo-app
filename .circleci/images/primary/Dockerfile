FROM circleci/node:8.0
USER root

RUN mkdir /home/node/.npm-global && chown -R root:root /root
ENV PATH=/home/node/.npm-global/bin:$PATH
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global

RUN sudo npm i -g npm-init -y && chown -R root:root /root
RUN sudo npm install --save-dev cypress && chown -R root:root /root
RUN chown -R root /node_modules/is-promise/package.json
RUN chown -R root /node_modules/is-promise
