
### `@Class Rule` 
[Fonte](https://junit.org/junit4/javadoc/4.12/org/junit/ClassRule.html)
feita para conseguir criar regras de uso antes da execução de um teste, como a conexão com um db antes e a desconexão depois do teste.

### `@DynamicPropertySource`

[fonte](https://docs-spring-io.translate.goog/spring-framework/reference/testing/annotations/integration-spring/annotation-dynamicpropertysource.html?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=tc)

uma anotação que pode ser aplicada a métodos em classes de teste de integração que precisam registrar propriedades _dinâmicas_ a serem adicionadas


### `@Testcontainers`

[fonte](https://docs-spring-io.translate.goog/spring-boot/reference/testing/testcontainers.html?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=tc)

A biblioteca [Testcontainers](https://translate.google.com/website?sl=en&tl=pt&hl=pt&client=srp&u=https://www.testcontainers.org/) oferece uma maneira de gerenciar serviços executados dentro de contêineres Docker. Ela se integra ao JUnit, permitindo que você escreva uma classe de teste que pode iniciar um contêiner antes da execução de qualquer teste. O Testcontainers é especialmente útil para escrever testes de integração que interagem com um serviço de backend real, como MySQL, MongoDB, Cassandra e outros.

Um padrão comum no Testcontainers é declarar as instâncias do contêiner como campos estáticos em uma interface.

```
import org.testcontainers.junit.jupiter.Container;
import org.testcontainers.mongodb.MongoDBContainer;
import org.testcontainers.neo4j.Neo4jContainer;

interface MyContainers {

	@Container
	MongoDBContainer mongoContainer = new MongoDBContainer("mongo:5.0");

	@Container
	Neo4jContainer neo4jContainer = new Neo4jContainer("neo4j:5");

}
```

### `@ResponseStatus`
Com a anotação ResponseStatus em cima de um controller conseguimos descrever oque queremos que ela retorne confome a execução dela, 200, 201 e por ai vai