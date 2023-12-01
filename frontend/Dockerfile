FROM node:18.18.0-alpine

# Add user
ENV USER dov_frontend
RUN adduser -D -g "" $USER

WORKDIR /dov/frontend
COPY package.json package-lock.json ./
RUN npm install --legacy-peer-deps
COPY ./ ./

USER $USER
EXPOSE 3000

CMD ["yarn", "start"]