FROM node:14 AS Production

ENV NODE_ENV=Production 

WORKDIR /usr/src/api

COPY ./api/package.json .
COPY ./api/package-lock.json .
RUN npm install 
COPY . .
RUN npm run build 
CMD ["sh", "-c", "npm run start:production"]
