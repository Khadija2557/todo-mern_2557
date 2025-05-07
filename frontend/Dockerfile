FROM node:18-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

# Optional: only build if you want static files, but remove it if using react-scripts start
# RUN npm run build

EXPOSE 3000

# This line is the fix: forces React dev server to bind to 0.0.0.0 so it's accessible from outside the container
CMD ["sh", "-c", "HOST=0.0.0.0 npm start"]

