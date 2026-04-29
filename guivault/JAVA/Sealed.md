[FONTE](https://www.baeldung.com/java-sealed-classes-interfaces)

**A Sealed permite que classes e interfaces definam seus subtipos permitidos.** Em outras palavras, uma classe ou interface pode definir quais classes podem implementá-la ou estendê-la. É um recurso útil para modelagem de domínio e aumento da segurança das bibliotecas.

sealed define um contrato fechado que modela variações de um mesmo conceito de domínio, garantindo que apenas tipos autorizados representem esse conceito