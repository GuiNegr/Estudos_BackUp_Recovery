## 🔹 O que é Polling (o “básico”)

**Polling** (ou _short polling_) é isso aqui:

1. Cliente faz requisição HTTP
2. Servidor responde imediatamente (tem dado ou não)
3. Cliente espera um tempo (ex: 5s)
4. Repete o processo

Exemplo mental:

Cliente: tem mensagem nova?  
Servidor: não  
(5 segundos depois)  
Cliente: tem mensagem nova?  
Servidor: não  
...

👉 Isso é literalmente um “loop de perguntas”.

- Muitas requisições inúteis
- Alto custo de rede e servidor
- Latência artificial (você só descobre algo no próximo ciclo)
- Escala mal em sistemas grandes
