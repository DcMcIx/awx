
# AWX Deploy - Single Node

Playbook for AWX deployment on a single node with k3s
## Author

- [@DcMcIx](https://www.github.com/DcMcIx)


## Deployment

To deploy AWX make sure you have ansible installed :

Playbook execution: 

```bash
ansible-playbook DEPLOY_AWX_Single_Node.yml
```


Custom EE with PY39 : docker.io/dcmcix/py39-awx-ee:latest

Custom EE with PY38 : docker.io/dcmcix/awx-ee:latest