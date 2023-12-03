FROM node:18-alpine

ENV USER dov_frontend
RUN adduser -D -g "" $USER

WORKDIR /dov/frontend

COPY ./ ./
RUN chown -R $USER /dov/frontend

USER $USER

# Yarn cache 디렉토리 설정
ENV YARN_CACHE_FOLDER=/dov/frontend/.yarn_cache
RUN mkdir -p $YARN_CACHE_FOLDER
RUN chown -R $USER $YARN_CACHE_FOLDER

RUN yarn install

EXPOSE 3000

CMD ["yarn", "start"]

