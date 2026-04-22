ao utilizar anotações com produces, podemos mostrar como queremos retornar nossa requisição em nossos serviços.., asim sendo na aplicação reativida quando fazemos 


```
@GetMapping(produces = MediaType.TEXT_EVENT_STREAM_VALUE)  
public Flux<EventoDto> getAllObjects(){  
    return serviceEvento.gettAll();  
}
```

estamos construindo um endpoint reativo. Significa que: ao fazer a requisição a conexão fica aberta pois ainda está acontecendo o fluxo. programação e endpoint reativo, consiste em trabalhar com fluxos que desecadeiam ações que podem afetar outros componetnes, assim quando algo entra no fluxo, ele só é parado quando completa ou quando falha.

não que a conexão fica aberta para sempre, A conexão fica aberta **enquanto o Flux ainda está emitindo eventos**.  
Se o Flux for finito (ex: dados do banco), ela fecha naturalmente.  
Se for infinito (ex: `Flux.interval`), ela permanece aberta até cancelament