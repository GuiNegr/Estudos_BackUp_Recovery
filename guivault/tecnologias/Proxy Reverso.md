a construção de um proxy reverso, ele pode fazer um load balancing porém ele é  uma ferramenta que executa  uma estrategia de distribuição. a ideia é ele ficar entre o cliente e o servidor, fazendo assim construções para redirecionamento. por exemplo: cachear conteúdos públicos e evitar cache em rotas autenticadas.
Um proxy reverso fica  atuando como ponto de entrada para as requisições. Ele pode executar funções como roteamento, cache, segurança e balanceamento de carga (implementando estratégias de distribuição).

Ele não lida com regras de negócio, como autenticação, mas pode tomar decisões baseadas em informações da requisição (headers, cookies, etc).

Um uso comum é cachear conteúdos públicos para reduzir carga no backend, enquanto evita cache em rotas autenticadas.


## Fluxo de uso.
como dito anteriormente o proxy reverso tem o objetivo de ser um ponto de entrada que aplica políticas de tráfego. o fluxo montado deve ser:

Cliente -> Proxy -> Aplicação -> Banco

|Camada|Responsabilidade|
|---|---|
|Cliente|envia request|
|Proxy reverso|roteamento, cache, segurança básica|
|Aplicação|regra de negócio (login, autorização)|
|Banco|persistência|

### Cache
O cache do proxy reverso armazena respostas HTTP para evitar requisições repetidas ao backend, sendo mais comum em conteúdos públicos e estáticos.

## Headers e cache
o proxy reverso precisa ficar de olho em seus headers de requisição, pois precisa entender se teve alguma mudança em relação as requisições que estão sendo encaminhadas. para mudar seu comportamento em relação aquele tipo de requisição. isso se torna uma medida de segurança afim de não cachear rotas com tokens de acesso

por exemplo: ao mandar uma requi com token de authorization, o proxy precisa entender que cachear aquilo pode ser um ponto de vazamento de dados


### Backend x Proxy reverso

O backend define as diretrizes de cache através de headers HTTP, indicando se e por quanto tempo uma resposta pode ser armazenada. No entanto, o proxy reverso é quem efetivamente implementa essas regras, podendo respeitá-las ou sobrescrevê-las dependendo da configuração. Por isso, o controle de cache é uma responsabilidade compartilhada entre backend e infraestrutur

Ref:
[Codigo fonte](https://www.youtube.com/watch?v=ngoEzjnJ2Eo)