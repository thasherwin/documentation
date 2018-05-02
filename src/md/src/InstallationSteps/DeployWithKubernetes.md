
## Deploy ReportPortal

ReportPortal can be easily deployed using Helm chart. 

In this instruction I will explain how to install Reportportal using Helm chart. These instruction are tested in Minikube with Kubernetes version 1.8.1

1. Clone the latest project from  [here](<https://github.com/reportportal/chart>) locally

2. Execute the following helm command 

  ```Shell
  helm install ./<report portal helm project folder>
  ```
  - If the commando is executed properly, you will see the following logs:
    ```Shell
    NAME:   boiling-quoll
    LAST DEPLOYED: Wed May  2 22:11:44 2018
    NAMESPACE: default
    STATUS: DEPLOYED
    
    RESOURCES:
    ==> v1/Service
    NAME           TYPE       CLUSTER-IP  EXTERNAL-IP  PORT(S)            AGE
    analyzer-0     ClusterIP  10.xxxxxx   <none>       8080/TCP           0s
    api-0          ClusterIP  10.xxxxxx   <none>       8080/TCP           0s
    elasticsearch  ClusterIP  None        <none>       55555/TCP          0s
    gateway        ClusterIP  10.xxxxxx   <none>       9998/TCP,9999/TCP  0s
    index-0        ClusterIP  10.xxxxxx   <none>       8090/TCP           0s
    mongodb        ClusterIP  10.xxxxxx   <none>       27017/TCP          0s
    registry       ClusterIP  10.xxxxxx   <none>       8500/TCP           0s
    uat-0          ClusterIP  10.xxxxxx   <none>       8080/TCP           0s
    ui-0           ClusterIP  10.xxxxxx   <none>       8080/TCP           0s
    
    ==> v1beta2/StatefulSet
    NAME           DESIRED  CURRENT  AGE
    analyzer       1        1        0s
    api            1        1        0s
    elasticsearch  1        1        0s
    gateway        1        1        0s
    index          1        1        0s
    mongodb        1        1        0s
    registry       1        1        0s
    uat            1        1        0s
    ui             1        1        0s
    
    ==> v1beta1/Ingress
    NAME                          HOSTS                ADDRESS  PORTS  AGE
    reportportal-gateway-ingress  reportportal.k8.com  80       0s
    
    ==> v1/Pod(related)
    NAME             READY  STATUS             RESTARTS  AGE
    analyzer-0       0/1    ContainerCreating  0         0s
    api-0            0/1    ContainerCreating  0         0s
    elasticsearch-0  0/1    ContainerCreating  0         0s
    gateway-0        0/1    ContainerCreating  0         0s
    index-0          0/1    ContainerCreating  0         0s
    mongodb-0        0/1    Pending            0         0s
    registry-0       0/1    Pending            0         0s
    uat-0            0/1    Pending            0         0s
    ui-0             0/1    Pending            0         0s
    ``` 
3. By default 


