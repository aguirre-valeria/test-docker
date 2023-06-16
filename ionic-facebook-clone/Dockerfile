# Etapa 1: Construye la imagen y instala las dependencias
FROM node:14-alpine AS builder

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia el archivo package.json y package-lock.json al directorio de trabajo
COPY package*.json ./

# Instala las dependencias del proyecto
RUN npm install

# Etapa 2: Copia los archivos al contenedor de la imagen de Ionic 5
FROM chiticariu/ionic5:latest

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia los archivos necesarios desde la etapa anterior
COPY --from=builder /app/node_modules ./node_modules
COPY . .

# Expone el puerto 8100 para acceder a la aplicación Ionic
EXPOSE 8100

# Inicia el servidor de desarrollo de Ionic
CMD ["npm", "run", "ionic:start"]