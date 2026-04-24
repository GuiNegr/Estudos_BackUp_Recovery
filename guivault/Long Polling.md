Basicamente o usuario manda uma chamada ao servidor que a segura em aberto até ter uma resposta ou ate o tempo de conexão fechar, caso ele consiga a resposta, ele encaminha de volta imedietamente e o cliente responde rapidatemente abrindo assim uma nova conexão e repetindo o processo.

Em sistemas que são construindo para monitoria ou sincronização de dados, esse tipo de conexão é utilizada, ela possui uma boa compatibilidade e facil implementação porém possui como problema a escalabilidade e a latencia.

![[longPolling.png]]