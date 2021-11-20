FROM node:alpine
#FROM: localhost:5000/node:alpine
#FROM: localhost:5000/node

ENV NODE_OPTIONS=--openssl-legacy-provider

COPY ./frontend /frontend

WORKDIR /frontend

#COPY package.json .

#COPY . .

#RUN npm install
RUN yarn add codecov --frozen-lockfile --network-timeout 100000
RUN yarn install --frozen-lockfile --network-timeout 100000

#COPY . .

EXPOSE 3000

CMD ["npm", "start"]
