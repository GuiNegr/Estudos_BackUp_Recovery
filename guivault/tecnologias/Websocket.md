Fontes:
[Websocket mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)
[Codigo fonte tv](https://www.youtube.com/watch?v=T4unNrKogSA)


WebSocket é um protocolo que estabelece uma conexão persistente e bidirecional entre cliente e servidor, permitindo que ambos enviem dados em tempo real sem a necessidade de múltiplas requisições HTTP.

Ele é um **protocolo próprio (ws / wss)** que começa como HTTP e depois **faz um upgrade** para um canal persistente.

Fluxo real:

1. Cliente faz uma requisição HTTP com `Upgrade: websocket`
2. Servidor aceita o upgrade (status `101 Switching Protocols`)
3. A partir daí:
    - não existe mais request/response
    - existe um **canal contínuo de troca de mensagens**

## Como os dados trafegam (frames)

Depois do upgrade, tudo vira **frames binários**:

Tipos principais:

- text (JSON normalmente)
- binary
- ping / pong (keep alive)
- close

![[Pasted image 20260423204812.png]]