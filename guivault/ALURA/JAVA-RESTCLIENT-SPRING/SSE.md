No SSE, o cliente inicia uma requisição HTTP para um endpoint e mantém a conexão aberta. A partir disso, o servidor envia eventos de forma contínua ou sob demanda, em um fluxo unidirecional (servidor → cliente), até que a conexão seja encerrada pelo cliente, pelo servidor ou por timeout.

![[sse.png]]