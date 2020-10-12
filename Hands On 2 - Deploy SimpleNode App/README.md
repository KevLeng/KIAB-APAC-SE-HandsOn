# HandsOn 2 : Deploy SimpleNode App


### Instructions

1.   Go to the simplenode directory:


     ```bash
     cd ~/kubernetes-deepdive/simplenode
     ```

1.   Create the deployment and the Service:

     ```bash
     sudo ./deploysimplenode.sh 
	 ```
 
1.   Check the Ingress and access the app: 

     ```bash
     kubectl get ing -n workshop
     
	 ```

1.   Access the application and click around to generate some traffic:

	 ```bash
	 sudo bash -c './keptn-in-a-box.sh &'
	 ```

![SimpleNodeApp](/img/simple-node-app.PNG)
