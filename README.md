# k8s
example object types 

Objects serves different purposes running a container, monitoring container, setting up networking etc 


StatefulSet -
ReplicationController-
Pod - runs one or more closely related containers
Service - setting up a networking, in Kubernetes C;luster

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

port mapping is require a lot of things  even if we gonna expose a port inside a pod spec it's gonna  open a port 3000 to the outside world 
to do so, you have to run a Service object type 


they have a metadata which 

SERVICES - WHEN we wanna set networking in Kubernetes Cluster
ClusterIP
Nodeport- Exposes a CONTAINER to the, outside world , as a dev open my browser and access from the browser, it's good only for the Dev purposes we don't use it in production 
 
 you and I would like to  open our browser and open a multi-client container from the browser which is in the pod,

 When we create a service object and set up a Service Nodeport - it's going to make a communication between the  multi-client container and the outside world 

 kubeproxy -one single window to the outside world in the Node, like a loadbalancer , which connect talks to services and does the described job .





Load Balancer 


INGRESS 






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


how the service nodeport - will expose port 3000 in a multi-client app? 
that when selector comes in on a Service object/ How service object is going to expose port 3000 on pod object, it's going to match with the service selector and the pods label and if the component - like (web) matches it's going to expose 3000  or match any other services 


the main reason using Nodeport service is to expose 3000 on web browser and make our multi client application work, how it's going to expose it's going have a matching selector within the service and it's going to search for the label within the pod and if they are going to match it's going to enable from the web browser to access our containeraized application! 

SERVICE Nodeport is has other ports as well 
port - if the other POD that need to connect our  multi-client pod will be able to connect though the Nodeport service ----port 
targetpod - is gonna have the same as multi client application containerport they way , it means that we want any incoming traffic send traffic to port 3000, and it's gonna mapped up to multi client container 
nodePort - has a range (30000-32767) is probably care most the important one because you and I are going to use it i will be accessing it inside my browser they way to be able to test it and we will specify the port number they way to be able to access it 