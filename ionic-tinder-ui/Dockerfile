# Usa la imagen de ionic3
FROM sevenn/ionic3:latest

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia los archivos del proyecto al directorio de trabajo
COPY . .

# Instala las dependencias del proyecto
RUN npm install

# Expone el puerto 8100 para acceder a la aplicación Ionic
EXPOSE 8100

# Inicia la aplicación Ionic
CMD ["ionic", "serve"]
