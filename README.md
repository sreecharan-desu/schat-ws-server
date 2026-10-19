# schat-ws-server

websocket server behind [schat](https://github.com/sreecharan-desu/schat).

## features

- broadcasts each valid message (`id`, `name`, `message`) to every client with a timestamp
- online-user count pushed on connect and disconnect
- heartbeat with ping/pong and a client cap

## stack

node · typescript · ws · docker

## run locally

```bash
npm install
cp .env.example .env
npm run dev          # ts-node, listens on PORT (8080 in .env.example, 3000 if unset)
npm run build && npm start
```

docker: `docker build -t schat-ws . && docker run -p 3000:3000 schat-ws`

## env

optional `PORT`. `.env.example` sets 8080, which is what schat expects by default.
