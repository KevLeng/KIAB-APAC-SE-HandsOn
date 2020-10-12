# HandsOn 2 : Deploy SimpleNode App


### Instructions

1.   Go to the simplenode directory:


     ```bash
     $ cd ~/kubernetes-deepdive/simplenode
     ```

1.   Create the deployment and the Service:

     ```bash
	 $ sudo ./deploysimplenode.sh
	 
     [sudo] password for dynatrace:
     namespace/workshop created
     deployment.apps/simplenode created
     service/simplenode exposed
     ingress.extensions/simplenode-ingress created
	 ```
 
1.   Check the Ingress and access the app: 

     ```bash
     $ kubectl get ing -n workshop
     
	 NAME                 CLASS    HOSTS                               ADDRESS     PORTS     AGE
     simplenode-ingress   <none>   simplenode.xxx-xxx-xxx-xxx.nip.io   127.0.0.1   80, 443   2m31s

	 ```

1.   Access the application and click around to generate some traffic:

     ![SimpleNodeApp](/img/simple-node-app.PNG)

1.   Find the service in Dynatrace and tag with "evalservice"

     ![SimpleNodeApp Service](/img/simple-node-app-service.PNG)

