# CHAT SERVICE

### STACK: Express.js, Typescript, REDIS, PostgreSQL, Socket.IO

Chat Service is a server-side chat system built with Express.js, TypeScript, PostgreSQL, Redis, and Socket.IO.

Messages are sent and deleted via HTTP requests, while Socket.IO is used to support real-time updates.
Data is stored in PostgreSQL, with Redis used for caching and performance optimization.

The service is scalable and ready for integration with client applications.

## LAUNCH

Installing dependencies
```bash
npm install
```

Building and running
```bash
npm run start
```

Linter code
```bash
npm run lint:fix
```

## STRUCTURE

```
AUTHSERVICE
└── src
    ├── config
    │   ├── app.config.ts
    │   ├── db.ts
    │   └── redis.config.ts
    ├── controllers
    │   └── chatController.ts
    ├── middleware
    │   └── authMiddleware.ts
    ├── routes
    │   └── ChatRoutes.ts
    ├── types
    │   └── socket.ts
    ├── utils
    │   └── chatSocket.ts
    ├── selfsigned_key.pem
    ├── selfsigned.pem
    └── server.ts
├── .env
├── .gitignore
├── eslint.config.mjs
├── package.json
├── README.md
└── tsconfig.json
```

## API ENDPOINTS

|Method | Path                  | Description                                   |
|-------|-----------------------|-----------------------------------------------|
| GET   | `/chats/:id/messages` | Получение сообщений в чате по токену (:id)    |
| POST  | `/chats/:id/messages` | Отправка сообщений в чат (:id)                |
| DELETE| `/message/?id=`       | Удаление сообщения                            |


## EXAMPLE .env
```
ACCESS_TOKEN_SECRET=
REFRESH_TOKEN_SECRET=
CHATPORT=
FRONTENDADDRES=
DB_HOST=
DB_USER=
DB_NAME=
DB_PASSWORD=
DB_PORT=
REDIS_HOST=
REDIS_PORT=
REDIS_PASSWORD=
```