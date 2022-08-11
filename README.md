
### CKA Certification 

## Architecture of Kubernetes

### kube-api server

'E resposonsavel por 


api-server 'e o unico componente que interage diretamento com o ETCD


Autenticar no cluster, Validar a request recuperar dados, atualizar o ETCD, Scheduler de tasks, e comunicar com o kubelet



Os certificados sao utilizados para proiteger a comunicacao entre os componentes 



use de kubeadm para caregar as configuracoes de cluster, eu posso configurar o cluster usando a api do kube-api ou posso usar o kubeadm

dentro do arquivo: /etc/kubernetes/manifests/kube-apiserver.yaml poomos ver todas as infos sobre nosso cluster

 voce pode listar o processo do api server com um:
 ps -aux | grep kube-apiserver

### kube controller-manager

Monitora o que acontece no cluster, quando subirmos um container, quando baixamos um container, monitora que o sistema esteja funcionando da forma desejada


Para um n'o ficar como UNREACHABLE 'e necessario que ele fiquei 40s sem se comunicar com o node-controller depois disso ele eh marcado como 


### Kube-scheduler

Resposavel pelo agendamento de pods nos nos. Ele apenas decide que pode vai para qual node.

Ele examina os nodes para validar em qual NODE o pod se encaixa melhor para ser executado.

As configuracoes do kube-scheduler, tamb'em podem ser vistas no arquivo: /etc/kubernetes/manifests/




### Kubelet 

 Ele 'e o capitao ele quem cria os pods nos nodes 

