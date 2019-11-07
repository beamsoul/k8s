# k8s
example object types 

Objects serves different purposes running a container, monitoring container, setting up networking etc 


StatefulSet -
ReplicationController-
Pod -
Service - setting up a networking,

when we specify a apiVersion that scoops  an object type, It's gonna open a access for the predefined sets of available objects for the apiversion. 
ConfigMaps 
Event
Pods 
Namespaces
Endpoint
component status 

apps/v1 -different 
controllerrevison 
Statefulset - 
it's gonna check the config file and decide what type of object it's gonna create,look up api version and stick it to api version.


Pods - grouping a containers that are related to each other, common purpose 

smallest unit we can deploy, 
requirement - we must run one or multiple container together 

PODS -is grouping related positively related containers together 
pods - we have containers that have to exxecuted together, tightly decoupled 


we cant deploy induvidual containers as wwe could with the docker compose 
others containers have a very 

































Service - we  create service object for the network purposes
1- Cluster IP -default one 
2- NodePort -
3  Load Balancer -
4  ExternalName- 


Master consist 
APi server
Control Manager
ETCD 
scheduler 


worker nodes 

Container runtime 
Kubeproxy - load balancer distributes the traffic to the PODS
Kubelet - agent between API server and Worker nodes 

