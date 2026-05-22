Kubernetes é um sistema de orquestração de containers que opera sobre um cluster (conjunto de máquinas).  
Ele é dividido em control plane, responsável por definir e manter o estado desejado do sistema, e worker nodes, que executam os workloads.  
O API Server é o ponto central de entrada e leitura do estado do cluster.  
O etcd armazena esse estado.  
O scheduler decide em qual node os pods serão executados.  
Os controllers observam continuamente os recursos do cluster e garantem que o estado atual corresponda ao estado desejado.


## Namespaces -> são separações de trabalhos dentro do seu ambiente, onde pode ser agrupado um cluster que pode ser utilizado para fazer deploy de pod da suas aplicações.

### Kubetelet -> ferramaneta utilizada pelos nó workers que náo possuem todo o acesso de api apenas as ferramentas utilizadas para ter visibilidade do health do seu pod.




[DOC KUBERNETES](https://kubernetes.io/docs/home/)
[DOC MINIKUBE PARA RODAR O KUBERNETS](https://minikube.sigs.k8s.io/docs/start/?arch=%2Flinux%2Fx86-64%2Fstable%2Fbinary%20download)
[DOC KUBECTL LINHA DE COMANDO DO KUBERNETES](https://kubernetes.io/pt-br/docs/reference/kubectl/)