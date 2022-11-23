FROM node:latest

WORKDIR /usr/src/app
RUN npm install mysql

COPY . .

EXPOSE 3000

ENTRYPOINT [ "npm", "run", "dev"]
# CMD ["node", "index.js"]

# docker run --rm -it -v $(pwd)/:/usr/src/app -p 3000:3000 node:latest bash
