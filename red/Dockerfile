###################################################################
# This is templating file of Dockerfile. It will help you to      #
# complete all required instructions for building the Dockerfile. #
###################################################################

# 1.1.1 | Use the following base image "node:17.0-alpine3.14"

FROM node:17.0-alpine3.14

# 1.1.2 | Working directory inside the containers should be "/app"

WORKDIR /app

# 1.1.3 | Copy "package*.json" file(s) to working directory

COPY package*.json ./

# 1.1.4 | Install "npm=7.17.0-r0" package manager, then install dependency packages

RUN npm install

# 1.1.5 | Copy "app.js" file to working directory

COPY app.js ./

# 1.1.6 | Copy the "index.pug" and "favicon.ico" files to the "/app/views" directory

RUN mkdir -p views
COPY index.pug ./views
COPY favicon.ico ./views

# 1.1.7 | The port "3000" should be exposed by the container

EXPOSE 3000

# 1.1.8 | The container must execute the command "node app.js" in run time

CMD ["node", "app.js"]