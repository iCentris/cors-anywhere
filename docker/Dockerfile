FROM node:14

# Create app directory
WORKDIR /app/src
COPY src/ /app/src 

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
# COPY package*.json ./

# RUN npm install
# If you are building your code for production
RUN apk add --no-cache vim python3 coreutils \
      bash openssh curl tar \
      linux-headers make python3-dev \
      gcc libc-dev libffi-dev groff less

RUN pip3 install --upgrade pip awscli &&\
    npm install -g npm@latest leo-cli@2.6.2

RUN npm -g install
#RUN npm ci --only=production

# Bundle app source
#COPY . .
EXPOSE 8080
CMD [ "node", "server.js" ]


