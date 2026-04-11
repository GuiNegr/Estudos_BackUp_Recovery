[Microservices](https://microservices-io.translate.goog/patterns/data/saga.html?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=tc)
[Dev.to](https://dev.to/thiagosilva95/saga-pattern-para-microservices-2pb6)
[Baeldung](https://www-baeldung-com.translate.goog/cs/saga-pattern-microservices?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=tc)

a ideia do saga pattern é garantir o ACID em toda seu ciclo de aplicações. um exemplo utilizado e no caso de um sistema de ECommerce, caso uma etapa falhe os outros micro serviços precisam estar prontos para falhar também. a ideia aqui é garantir ou o SUCESSO TOTAL ou a FALHA TOTAL da saga do usuario. por exemplo, 

usuario compra -> verifica se há no estoque -> verifica se pode encaminhar -> fatura no cartão do usuario

se a caso um step falhar desse ciclo, todos os demais devem falhar.
