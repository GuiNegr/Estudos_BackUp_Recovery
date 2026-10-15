
# Conceitos de Nuvem.
Scale Vertical:
E quando voce adiciona mais recursos a maquina, quando redimensionada precisa ser reiniciada.

Scale Horizontal
quando voce adiciona mais maquinas para sua aplicação.

Sticky Sessions.
Quando utilizamos o scale Horizontal nos deparamos com  a seguinte situação: varias maquinas um usuario, o objetivo do sticky sessions é gerar um cookie para seu backend vinculando aquele usuario a uma instancia

apesar das capaciades de scales falarem sobre aumentar o quanto sua aplicação pode aguentar, há um ponto importante. em Horizontal Scales,  você perde por um momento sua aplicação pois ela irá precisar de um restart 

(um adendo sobre esse caso. perguntar no trabalho ao Pavão se a combinação de um scale horizontal junto com as aplicações que usam build nativo é algo interessante, visto que essas aplicações tem um Warmup mais rapido.)

# EC2
### Tipos de instancias.

- Uso geral:
- Otimizada para computação:
- Otimizada para memória:
- Computação acelerada:
- Otimizada para armazenamento:

# Glossario.
EC2 -> Amazon Elastic Compute Cloud.
Multitancy -> Quando multiplicas instancias compartilhar o mesmo host
AMI -> Maquina de imagem amazon para instancias EC2




# AWS Cloud Watch
utilizado para capturar metricas das instancias da aws


# Filas da amazon

## SQS
PODE ESPERAR ALGUÉM VIR BUSCAR

## SNS
TEM QUE TER ALGO PARA ENVIAR/RECEBERF IMEDIATAMENTE




# Domain 1 Review AWS


AWS Well architeture framework
são um conjuto de boas praticas que devem ser utilizadas como para a criação de arquiteturas de sistemas dependentes das ferramentas que tangem a AWS

aws snowball edge é utilizado para migração de grande quantidade de dados
