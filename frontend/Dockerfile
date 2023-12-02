FROM node:18.18.0-alpine

WORKDIR /dov/frontend
COPY package.json package-lock.json ./
RUN yarn install
COPY ./ ./

EXPOSE 3000

CMD ["yarn", "start"]
