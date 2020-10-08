# HandsOn 1 : Install Keptn - Manual

### Prerequisites
You will need:

* Tenant URL: e.g.  ```https://<server name>/e/<environment id>```
* PaaS Token
* API Token

API Token needs the following permissions:

![API Permissions](/img/api-token-img.png)

----

### Instructions

1.   First clone KIAB repo:


     ```bash
     git clone --branch release-0.7.1 https://github.com/keptn-sandbox/keptn-in-a-box
     ```

1.   Change directories:

     ```bash
     cd keptn-in-a-box/
	 ```
 
1.   In file **keptn-in-a-box.sh**. Set TENANT=,PAASTOKEN=,APITOKEN= to your environment details. Also add jenkins_deploy=true to the specific function section.
You can edit file directly or used commands like the following: 

     ```bash
     export TENANT=<TENANT-URL>
     export PAASTOKEN=<PAAS-TOKEN>
     export APITOKEN=<API-TOKEN>
     
     sed -i -e 's~TENANT=~'"TENANT=$TENANT"'~' -e 's~PAASTOKEN=~'"PAASTOKEN=$PAASTOKEN"'~' -e 's~APITOKEN=~'"APITOKEN=$APITOKEN"'~' -e 's~#create_workshop_user=true~jenkins_deploy=true~' keptn-in-a-box.sh
	 ```

1.   Run installer script as sudo:

	 ```bash
	 sudo bash -c './keptn-in-a-box.sh &'
	 ```

1.   You can check the progess by looking at the /tmp/install.log

	 ```bash
	 tail -f /tmp/install.log
	 ```