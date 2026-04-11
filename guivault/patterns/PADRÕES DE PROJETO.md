Padrões de projetos são uma visão arquitetural do seu problema. São problemas que já estiveram com uma forma de solucionar e assim descrita como um padrão para outros problemas, ao contrario de algoritmos que da uma forma passo a passo de como implementar eles, padrões de projeto são como uma planta do seu projeto, onde é capaz de observar de que forma o problema pode ser resolvido e cabe você a implementação da melhor forma para seu projeto.

## TIPOS DE PADRÕES
Há 3 tipos de padrões para seu projeto. são eles 

### Padrões **criacionais**.
Fornecem mecanismos de criação de objetos que aumentam a flexibilidade e a reutilização ed código. por exemplo:
	você possui um projeto que de uma padaria, a forma que vai construir o pão vai ser a mesma para o pão salgado e o pão doce, a abstração desse processo pode ser encapsulada em um padrão chamado factory.
	O **Factory Method** é um padrão criacional de projeto que fornece uma interface para criar objetos em uma superclasse, mas permite que as subclasses alterem o tipo de objetos que serão criados.

### Padrões Estruturais.
explicam como montar objetos e classes em estruturas maiores, enquanto ainda mantém as estruturas  flexíveis  e eficientes.  por exemplo Facade.
	voce tem 3 aplicações de contabildiade, uma coloca quanto voce gastou em uma planilha, outra faz o pagamento para um local x, e a outra te retorna seu extrato bancarios após o debito. antes você precisaria de 3 metodos chamando cada aplicação, porém voce pode criar uma interface entre que agrupe esses 3 para simplificar o retorno.
	O **Facade** é um padrão de projeto estrutural que fornece uma interface simplificada para uma biblioteca, um framework, ou qualquer conjunto complexo de classes.

### Padrão Comportamental. 
cuidam da comunicação eficiente e da assinalação de responsabilidades entre objetos.
por exemplo o Strategy. O **Strategy** é um padrão de projeto comportamental que permite que você defina uma família de algoritmos, coloque-os em classes separadas, e faça os objetos deles intercambiáveis.

### Outros padrões.
[[SAGA PATTERN]]

















Ref:
[Fonte refatcor guru](https://refactoring.guru/pt-br/design-patterns/classification)
