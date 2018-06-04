FROM circleci/node:8.11
USER root

RUN apt-get update && \
  apt-get install -y \
    libgtk2.0-0 \
    libnotify-dev \
    libgconf-2-4 \
    libnss3 \
    libxss1 \
    libasound2 \
    xvfb

RUN mkdir /home/node/.npm-global && chown -R root:root /root
ENV PATH=/home/node/.npm-global/bin:$PATH
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global

RUN sudo npm i -g npm-init -y && chown -R root:root /root
RUN sudo npm install --save-dev cypress && chown -R root:root /root
RUN ln -s /usr/bin/nodejs /usr/bin/node
