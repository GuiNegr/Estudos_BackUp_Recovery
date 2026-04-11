Kubernetes é um sistema de orquestração de containers que opera sobre um cluster (conjunto de máquinas).  
Ele é dividido em control plane, responsável por definir e manter o estado desejado do sistema, e worker nodes, que executam os workloads.  
O API Server é o ponto central de entrada e leitura do estado do cluster.  
O etcd armazena esse estado.  
O scheduler decide em qual node os pods serão executados.  
Os controllers observam continuamente os recursos do cluster e garantem que o estado atual corresponda ao estado desejado.