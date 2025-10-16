# 1. Since this isn't Python, our base image will be `node:14`
FROM node:14

WORKDIR /usr/src/app

COPY ./package.json ./
COPY ./public ./public
COPY ./src ./src
# 2. `pip` is for Python and we will be using `yarn` here so change the `pip install ...` command to `yarn install`
RUN yarn install 

EXPOSE 3000
# 3. Your final command to run the application should be `CMD ["yarn", "start"]` as the frontend runs when we use `yarn start`
CMD ["yarn", "start"]