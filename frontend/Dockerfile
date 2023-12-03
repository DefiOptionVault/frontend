FROM node:18-alpine

ENV USER dov_frontend
RUN adduser -D -g "" $USER

WORKDIR /dov/frontend

COPY ./ ./
RUN chown -R $USER /dov/frontend

RUN yarn install

USER $USER
EXPOSE 3000

CMD ["yarn", "start"]
