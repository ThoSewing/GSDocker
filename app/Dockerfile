# Use uma imagem base leve do Node.js
FROM node:14-alpine

# Defina o diretório de trabalho dentro do contêiner
WORKDIR /usr/src/app

# Copie os arquivos package.json e package-lock.json para o diretório de trabalho
COPY package*.json ./

# Instale as dependências da aplicação
RUN npm install --only=production

# Copie o código da aplicação para o diretório de trabalho
COPY . .

# Expõe a porta 8090 para que a aplicação possa ser acessada externamente
EXPOSE 8090

# Defina o usuário não-root para a execução da aplicação
USER node

# Comando para iniciar a aplicação quando o contêiner for iniciado
CMD ["node", "app.js"]

