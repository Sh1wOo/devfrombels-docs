---
sidebar_position: 1
---
# Server installing packages
```bash
git clone https://github.com/DevsFromBels/finance-app.git
```

### Setup Docker
```DockerFile
version: "3.9"
services:
  postgres:
    image: postgres:16
    environment:
      POSTGRES_DB: "finance_app"
      POSTGRES_USER: "fin_admin"
      POSTGRES_PASSWORD: "pgpwd4habr"
    ports:
      - "5432:5432"
```

### Setup .env
Rename __.env.example__ to __.env__ and format string for your docker enviroment
```.env
# Edit edit this for your machine
DATABASE_URL="postgresql://johndoe:randompassword@localhost:5432/mydb?schema=public"
```

### Installing Packages
With **npm**:
```bash
npm install
```
With **bun**:
```bash
bun install
```

### Createing DataBase 
```bash
sudo npx prisma db push
```