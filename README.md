# markdown-tips-and-tricks

This repo is also for me to experiment with how github markdown behaves

<details>
<summary> :question: </summary>
  <h2>I just learned about dropdowns (and emoji's)</h2>
<br>
From here : https://gist.github.com/citrusui/07978f14b11adada364ff901e27c7f61 <br/>      
See also Emoji cheat sheet : https://www.webpagefx.com/tools/emoji-cheat-sheet/
</details>
  
<br/>
<br/>
 
:information_source:
  
:warning:
  
  
-----------




# Supporting Platform i2i


This documentation is intended for **Project i2i Support Personnel**.     

It outlines the tools and processes available for investigating any issues with the platform.

This document is to be used in conjunction with the **[i2i Business Continuity Plan](https://consensys.quip.com/Nfu9A6RPmHeT/Business-Continuity-Plan)**.     

<br/>


---

## Pre-Setup Steps 

#### Obtain access to services
<details>
<summary> How to obtain the access you need </summary>
<br/>
You will need to reach out to the i2i Dev Ops to gain access to the various systems.<br/>
See the <a target="_blank" href="https://consensys.quip.com/Nfu9A6RPmHeT/Business-Continuity-Plan">Business Continuity Plan</a> for how to reach the <a href="https://consensys.quip.com/Nfu9A6RPmHeT#VCUACAjUWaX" target="_blank">DevOps</a> or <a href="https://consensys.quip.com/Nfu9A6RPmHeT#VCUACAE5MuE" target="_blank">i2i support team</a>.<br/>
</details>


#### Links to services
<details>
<summary> Azure / Kaleido / Github / 1Password / Quip </summary>

* Azure (and CosmosDB) : <https://portal.azure.com/>
* Kaleido (blockchain) : <https://console-ap.kaleido.io/login>
* Github repo : <https://github.com/ConsenSys/siargao> (you probably have this already)
* 1 Password (secrets files) : <https://consensys.1password.com/signin>
* Quip (ConsenSys documents): email Help Desk <helpdesk@consensys.net>
</details>



#### KUBECONFIG file
<details>
<summary> How to meet the "KUBECONFIG file" requirement </summary>
<br/>
You will need to reach out to the i2i Dev Ops to get your personal kubernetes configuration file created.<br/>
<br/>
The file will be pasted into 1Password and you can download it from there and save it as `~/.kube/my-cube-config`.<br/>
<br/>
(NB: you can call it `~/.kube/config` and leave out the `KUBECONFIG=~/.kube/my-cube-config` part of all the kubernetes commands listed here)
</details>


#### Azure whitelisted IP
<details>
<summary> How to meet the "Azure whitelisted IP" requirement </summary>
<br/>
You will need to first get the i2i Dev Ops to set up whitelist rules for you, after that you can modify your own rule to match your current IP address.<br/>
<br/>
To whitelist your IP for access to <u>kubernetes tools</u> : <br/>
<b>Azure portal > Resource groups > </b>[ "APAC-Siargao-Production" (<b>Live</b>) | "APAC-Siargao-Preprod" (<b>Dev, Test, or Stage</b>) ]<b> > k8s-master-xxxxx-nsg (Network security group) > (your name) > Modify "Source IP addresses"  </b><br/>
<br/>
To whitelist your IP for access to <u>CosmosDB</u> (NB: not needed for dev or test) : <br/>
<b>Azure portal > Resource groups > </b>[ "APAC-Siargao-Production" (<b>Live</b>) | "APAC-Siargao-Preprod" (<b>Stage</b>) ]<b> > [ siargao-db-prod | siargao-db-stage ] > Firewall and virtual network > Add "IP (SINGLE IPV4 OR CIDR RANGE)" </b><br/>
<br/>
To whitelist your IP for access to <u>Jenkins</u> : <br/>
<b>Azure portal > Resource groups > "APAC-Siargao-Shared" > jenkins-nsg (Network security group) > (your name) > Modify "Source IP addresses" </b><br/>
<br/>
<i>Hint 1 : You can optain your public IP by googling "whats my ip"</i><br/>
<i>Hint 2 : After you choose your resource group, select "Group by type" in the top-right to make it easier to find the service you need</i>
</details>


#### More detailed information
<details>
<summary> To learn more about anything technical related to i2i </summary>
<br/>
There are detailed articles on all of the i2i infrastructure technologies in both Quip and the Github repository. <br/> 
A good index to these articles exists in the Business Continunity Plan :<br/>
<br/>
In the <a href="https://consensys.quip.com/Nfu9A6RPmHeT#VCUACAcfT2D" target="_blank">"Essential i2i Technical Resources"</a> section there are links to detailed articles about: project i2i generally, Azure and the i2i enviornments, software components, error codes, access controls, and the different kinds of logs.<br/>
<br/>
In the <a href="https://consensys.quip.com/Nfu9A6RPmHeT#VCUACALPYsg" target="_blank">"Related i2i Technical Resources"</a> section of the BCP there are links to : github acces, where geographically data is stored, setting up a dev environment, code deployment and build processes, software version, infrastructure "how to" videos.
</details>


<br/>

-----



## Platform Health Check

* Dev : [https://dev-siargao.consensys.net/api/health](https://dev-siargao.consensys.net/api/health)
* Test (UAT) : [https://test-siargao.consensys.net/api/health](https://test-siargao.consensys.net/api/health)
* Stage : [https://stage-siargao.consensys.net/api/health](https://stage-siargao.consensys.net/api/health)
* Production : [https://siargao.consensys.net/api/health](https://siargao.consensys.net/api/health)     
   (But your IP must be whitelisted for prod??? LINK TO WHITELIST) 


## Viewing Logs

#### 

**Requires :** [Azure whitelisted IP](), [KUBECONFIG file](#kubeconfig-file), 


## Kubernetes Console


## Using the i2i CLI

... querying the database

... querying the chain 

... querying both using API end points ...

... Manual test chain connection 

```
CHAIN_RPC_STR=***YOU GET THIS, LIKE : https://a0gheozjlw:VHVHE2dzS9ksl2Uk4U5A9_YSF0HRi2zqbA5buqmTHd0@a0nsgrn8ka-a0d900ezfz-rpc.ap-southeast-2.kaleido.io***          
curl -sX POST --data '{"jsonrpc":"2.0","method":"admin_nodeInfo", "id":1}' $CHAIN_RPC_STR
```

misc notes ?? :  :

* Kubernets Console
* Logs
* CLI investigation tool 




See the 

