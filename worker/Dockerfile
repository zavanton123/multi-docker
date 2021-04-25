FROM node:alpine
WORKDIR "/app"
COPY ./package.json ./
RUN npm config set unsafe-perm true
RUN npm install --force
RUN chown node -R /app/node_modules
COPY . .
USER node
CMD ["npm", "run", "start"]
