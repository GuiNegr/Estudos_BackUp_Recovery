No spring há varios tipos de interfaces repositorys com finalidades e própositos diferentes para cada tipo de aplicação, seja ela reativa,sincrona ou que trablhe com dados que possue paginação. Assim a escolha de repository que deve ser usada, depende do contexto em que seu projeto está inserido.

geralmente utilizo a JPA. sem eu saber é claro, parece ser a mais completa em situações sincronas, já que ela combina a crudRepository(que é uma interface que possui apenas metodos relacionados ao padrão CRUD) ou PagingAndSortingRepository que utiliza metodos sofisticados para paginação e iteração de valores

para uso noSQL existe a MongoRepository 
e para uso reativo existe há  ReactiveCrudRepository

oque diferencia a conexão de um banco reativo, com um banco em aplicações sincronas?

as interfaces separadas são feitas pois a forma que será manipulada a thread/contexto são diferentes. no jpa padrão temos a execução de uma thread que chega e espera e devolve. já no reactive voce tem uma thread que inicia uma pipeline que pode ou não retornar um valor, isso não faz a thread ficar bloqueante.
