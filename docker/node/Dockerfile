FROM node:latest

WORKDIR /usr/src/app
RUN npm install mysql

# RUN touch docker-entrypoint.sh && \
#     echo "#!/bin/bash\nnode index.js" > docker-entrypoint.sh && \
#     chmod +x docker-entrypoint.sh

# install dockerize
RUN apt-get update && apt-get install -y wget
ENV DOCKERIZE_VERSION v0.6.1
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz

COPY . .

EXPOSE 3000

# ENTRYPOINT [ "npm", "run", "dev"]
# CMD ["node", "index.js"]

# docker run --rm -it -v $(pwd)/:/usr/src/app -p 3000:3000 node:latest bash
