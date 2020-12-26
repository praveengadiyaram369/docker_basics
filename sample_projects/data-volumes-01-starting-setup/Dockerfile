FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

# environment variables can be used inside the application code
#ENV PORT 80

EXPOSE 80

# inorder to store data permanently on our local machines, we use volumes 
# below is an example of anonymous volume where we do not specify any name, just the location.
# VOLUME [ "/app/feedback"]

CMD ["node", "server.js"]