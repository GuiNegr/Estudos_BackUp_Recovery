faz parte do uso da api Streams de java mais tem usos diferentes.
`map` transforma um valor direto;  
`flatMap` é usado quando a transformação já devolve um container e você precisa evitar aninhamento.

```

public Mono<EventoDto> getByID(Long id){  
    return repository.findById(id)  
            .switchIfEmpty(Mono.error(new ResponseStatusException(HttpStatus.NOT_FOUND)))  
            .map(EventoDto::toDTO);  
}
```

```

public Mono<EventoDto> update(EventoDto eventoDto,Long id) {  
  
    return repository.findById(id)  
            .switchIfEmpty(Mono.error(new ResponseStatusException(HttpStatus.NOT_FOUND))).flatMap(evento -> {  
                if(eventoDto.nome() != null && !eventoDto.nome().isBlank()){  
                    evento.setNome(eventoDto.nome());  
                };  
                if(eventoDto.data() != null){  
                    evento.setData(eventoDto.data());  
                };  
                if(eventoDto.tipo() != null){  
                    evento.setTipo(eventoDto.tipo());  
                }  
                if(eventoDto.descricao() != null && !eventoDto.descricao().isBlank()){  
                    evento.setDescricao(eventoDto.descricao());  
                }  
                EventoService.log.info("Update has sucessful!");  
            return repository.save(evento);  
    }  
    ).map(EventoDto::toDTO);  
  
}
```