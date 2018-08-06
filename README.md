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



#### Azure whitelisted IP
<details>
<summary> How to meet the "Azure whitelisted IP" requirement </summary>
<br/>
You will need to first get the i2i Dev Ops to set up whitelist rules for you, after that you can modify your own rule to match your current IP address.<br/>
<br/>
To whitelist your IP for access to <u>kubernetes tools</u> : <b> TODO ...</b><br/>
<br/>
To whitelist your IP for access to <u>CosmosDB</u> :arrow_right: <b>Azure portal :arrow_right: Resource groups :arrow_right: </b>[ "APAC-Siargao-Production" (<b>Live</b>) | "APAC-Siargao-Preprod" (<b>Dev, Test, or Stage</b>) ]<b> :arrow_right: k8s-master-xxxxx-nsg (Network security group) :arrow_right: (your name) :arrow_right: Modify "Source IP addresses"  </b><br/>
<br/>
To whitelist your IP for access to <u>Jenkins</u> : <b>Azure portal > Resource groups > "APAC-Siargao-Shared" > jenkins-nsg (Network security group) > (your name) > Modify "Source IP addresses" </b><br/>
<br/>
<i>Hint 1 : You can optain your public IP by googling "whats my ip"</i><br/>
<i>Hint 2 : After you choose your resource group, select "Group by type" in the top-right to make it easier to find the service you need</i>
</details>


**Requires :** [xxx](), [yy](#kubeconfig-file), 

## :black_small_square: Pre-Setup Steps 


#### KUBECONFIG file
<details>
<summary> How to meet the "KUBECONFIG file" requirement </summary>

Link to : <http://google.com> 


</details>
