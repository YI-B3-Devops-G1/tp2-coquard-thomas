#import de l'image node avec version lts-alpine depuis Dockerhub
FROM node:lts-slim


#Création du répertoire + modification du propriétaire de fichier
WORKDIR /home/node/app
COPY package*.json ./
RUN chown -R node:node /home/node/app && npm install

#Création utilisateur node
USER node

EXPOSE 8080

#lance le serveur node
CMD [ "npm", "run", "start" ]