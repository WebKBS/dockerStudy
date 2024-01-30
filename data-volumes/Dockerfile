FROM node


WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

ARG DEFAULT_PORT=80 
ENV PORT 80

EXPOSE $PORT

# VOLUME [ "/app/feedback" ]

CMD ["npm", "start"]

