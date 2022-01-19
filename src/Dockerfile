FROM node:14-alpine

# Especificando Diretório base da aplicação no container
WORKDIR /app

# Copiando o arquivo indexador dos modulos do node para a pasta de trabalho do container
COPY package*.json ./

# Executando a instalação dos pacotes
RUN npm install

# Copiando os arquivos da aplicação para o dirtetorio base da aplicação (Baseado em camadas para evitar execuções desnecessárias)
COPY . .

# Expondo a porta da aplicação
EXPOSE 8080

# Iniciando a aplicação via node
CMD [ "node", "server.js" ]