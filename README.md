
# AWX Deploy - Single Node

Playbook for AWX deployment on a single node with k3s
## Author

- [@DcMcIx](https://www.github.com/DcMcIx)


## Deployment

To deploy AWX make sure you have ansible installed and your inventory populated with the target server :

Playbook execution: 

```bash
ansible-playbook DEPLOY_AWX_Single_Node.yml
```
You can target your server by adding '--limit' flag :
```bash
ansible-playbook DEPLOY_AWX_Single_Node.yml --limit [SERVER_IP_OR_SERVER_NAME]
```


## Custom AWX-EE
You can use my custom EE (Including community.general and many other collections)

AWX-EE with PY39 :
```bash
docker.io/dcmcix/py39-awx-ee:latest
```
AWX-EE with PY38 :
```bash
docker.io/dcmcix/awx-ee:latest
```