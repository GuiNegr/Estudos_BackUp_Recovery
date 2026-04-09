+++
title = 'Entendo o JDBC  a fundo!'
date = '2026-02-09'
+++

# Como o JDBC FUNCIONA:
O JDBC é uma API que define um contrato entre aplicações Java e bancos de dados relacionais. Ele funciona acima de drivers específicos, que são responsáveis por implementar a comunicação real com o banco utilizando seu protocolo nativo.

Ao solicitar uma conexão via `getConnection`, o JDBC aciona o driver adequado, que abre um socket TCP com o servidor do banco de dados e inicia o handshake definido pelo protocolo do banco. Esse processo vai além de uma simples troca de mensagens, envolvendo autenticação, negociação de capacidades e validação da sessão.

Durante o handshake, o servidor envia um valor aleatório (salt) e informações sobre o método de autenticação. O driver utiliza esse salt para gerar uma representação criptográfica da senha, que é enviada ao servidor. O banco compara esse valor com o hash armazenado e, se houver correspondência, autentica o usuário.

Após a autenticação, a conexão permanece aberta por meio do socket, que atua como um canal persistente de comunicação. A partir desse ponto, o driver JDBC traduz chamadas da API Java em comandos do protocolo do banco e converte as respostas em tipos compreensíveis pela aplicação Java.


