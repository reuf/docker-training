FROM node:14.16.0-alpine3.13
RUN addgroup app && adduser -S -G app app
USER app
WORKDIR /app
RUN mkdir data
COPY package*.json .
RUN npm install
COPY . .
ENV API_URL=http://api.myapp.com
EXPOSE 3000
# Shell form - spins up a new shell, use never
# /bin/sh
# cmd
# CMD npm start

# Exec form - uses same shell to execute, use always
CMD ["npm", "start"]

# ENTRYPOINT ["npm","start"] - can also be used