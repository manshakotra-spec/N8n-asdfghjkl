n8n-render/
│── Dockerfile
│── docker-compose.yml
│── .env
│FROM n8nio/n8n

ENV N8N_PORT=10000
EXPOSE 10000version: "3"

services:
  n8n:
    image: n8nio/n8n
    restart: always
    ports:
      - "10000:10000"
    environment:
      - N8N_PORT=10000
      - N8N_HOST=0.0.0.0
      - WEBHOOK_URL=https://your-app.onrender.com/
      - GENERIC_TIMEZONE=Asia/Kolkata
    volumes:
      - n8n_data:/home/node/.n8n

volumes:
  n8n_data:N8N_BASIC_AUTH_ACTIVE=true
N8N_BASIC_AUTH_USER=admin
N8N_BASIC_AUTH_PASSWORD=strongpassword

# Optional DB (leave empty for now if beginner)
DB_TYPE=sqlite# n8n Render Deployment

## Deploy Steps
1. Upload this repo to GitHub
2. Go to Render
3. Create New Web Service
4. Connect repo
5. Select Docker
6. Deploy

## Default Login
User: admin
Password: strongpasswordDB_TYPE=postgresdb
DB_POSTGRESDB_HOST=your-host
DB_POSTGRESDB_DATABASE=postgres
DB_POSTGRESDB_USER=postgres
DB_POSTGRESDB_PASSWORD=your-password# n8n Render Deployment

## Deploy Steps
1. Upload this repo to GitHub
2. Go to Render
3. Create New Web Service
4. Connect repo
5. Select Docker
6. Deploy

## Default Login
User: admin
Password: strongpasswordnpm installn8nDockerfileFROM n8nio/n8n

EXPOSE 5678FROM n8nio/n8n

EXPOSE 5678── README.md
