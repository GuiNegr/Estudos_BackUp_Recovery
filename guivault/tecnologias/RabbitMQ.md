[Fonte](https://www.rabbitmq.com/docs)

RabbitMQ é um Message Broker, é um software que atua como intermediário entre diferentes aplicações ou serviços, facilitando a troca de mensagens de forma confiável e assíncrona.

ele da suporte a diversos protocolos, porém o principal é o 


## **MQTT**
> **_Message Queue Telemetry Transport_**

um protocolo para troca de mensagens em ambientes onde se tem alguma restrição de hardware, como pouca memória disponível, por exemplo, ou uma limitação de banda.
geralmente utilizado para IOT

## **STOMP**
> **_Simple (or Streaming) Text Oriented Message Protocol_**

[FONTE](https://stomp.github.io/)

é um protocolo baseado em texto, construído para trabalhar com _middlewares_ orientados à mensagem. Possui uma estrutura similar ao AMQP, com cabeçalho, propriedades e corpo da mensagem, porém não lida com tópicos ou filas. Ele usa uma semântica de string de destino.


## AMQP
> Advanced Messaging Queue Protocol

que é baseado no TCP

usa padrão de PUB -> SUB

ou seja: terá uma aplicação para publicar a mensagem e um subscriber para receber as mensagems.


### Exchange
são um tipo de intermedia que o publicador envio a mensagem, o objetivo dela é identififcar qual é  a fila que a mensagem deve ser encaminhada.
Há varios tipos. consultar a DOC para mais informações....
alguns são:f
- Default: basicamente é aque vem sem declaração, voce como um publisher apenas precisa dizer qual a fila que voce precisa encaminhar a mensagem
- Direct: quando voce precisa de uma Routing Key para conseguir direcionar as mensgems direatamente para quem possui as Routing Key.
- Fanout: Ignora a routing Key e envia para todos que possuem uma binding Key
- Topic: basicamente difinir rergas de como entregar as mensagem
- Header: envia baseado no cabeçalho.


Docker compose para se eu precisar em algum momento

lembrar de trocar a versão do rabbit
```yaml
version: "3.6"

services:
    rabbitmq:
        image: rabbitmq:3.10-management
        container_name: rabbitmq
        restart: always
        ports:
            - 5672:5672
            - 15672:15672
        volumes:
            - ./dados:/var/lib/rabbitmq/
        environment:
            - RABBITMQ_DEFAULT_USER=jacqueline
            - RABBITMQ_DEFAULT_PASS=alura
```


para rodar o comando docker e iniciar um container com o rabbit usar

```shell
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.10-management
```


# Channels
Channels cannot exist without a connection.
A channel only exists in the context of a connection and never on its own.Some applications need multiple logical connections to the broker. However, it is undesirable to keep many TCP connections open at the same time because doing so consumes system resources and makes it more difficult to configure **firewalls**. Every protocol operation performed by a client happens on a channel


# Topico
A topic uses a publish-subscribe (pub/sub) model. In this case, a message published to a topic is received by all subscribers.

# Queue
A **queue** follows a **point-to-point** communication model: messages are sent by a producer and consumed by **only one consumer**. Once a message is processed, it is removed from the queue.