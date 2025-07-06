# Use Node 23.10
FROM node:23.10

WORKDIR /app

COPY . .

RUN npm install
RUN npm run build

# Serve using static server
RUN npm install -g serve

EXPOSE 3000

CMD ["serve", "-s", "dist", "-l", "3000"]