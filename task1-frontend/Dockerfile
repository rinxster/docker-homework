FROM node:alpine

ENV NODE_OPTIONS=--openssl-legacy-provider

WORKDIR '/app'

COPY package.json .

#RUN npm install
RUN yarn add codecov --frozen-lockfile
RUN yarn install --frozen-lockfile --network-timeout 100000

COPY . .

EXPOSE 3000

CMD ["npm", "start"]