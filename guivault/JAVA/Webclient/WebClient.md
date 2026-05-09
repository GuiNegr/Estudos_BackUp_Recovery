Há varias libs para uso de webClient, como HTTPCLient, WebFlux, RestTemplate....
o objetivo delas é fornecer uma interface para o usuario conseguir de forma prática conseguir fazer chamadas a APIS externas já com metodos de construção para headers e transoformação de Bodys.

### Onde a magica de um metodo acontece.
sempre que visualizar uma linha webClient é o .exchange() que faz o envio da req