FROM node:14

# Create app directory
WORKDIR /app/src
COPY src/ /app/src 

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY src/package*.json ./

# RUN npm install
# If you are building your code for production


RUN npm install -g npm@latest

RUN npm -g install
#RUN npm ci --only=production

# Bundle app source
#COPY . .
EXPOSE 8080
CMD [ "node", "server.js" ]


