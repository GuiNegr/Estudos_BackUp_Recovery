para entender sobre precisamos ver primeiro [[servidores de aplicação]]

as principais diferenças entre o netty e o tomcat é a forma que é gerenciada a thread. enquanto o tomcat ele mantem a mesma trhead que inicou a request para devolve-la. o netty parte para algo mais dinamico, onde não há esse block de thread. quando miramos o uso do tomcat estamos em busca de um contexo syncrono que pode ter contextos bloqueantes.
a perca de contexto por conta da troca de trhead é um problema para sistemas reativos.