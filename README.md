Based on the deployment process from : https://github.com/ansible/awx-operator

After The Installation :

Get NodePort :

kubectl get svc -l "app.kubernetes.io/managed-by=awx-operator" | grep -i NodePort

Get admin Password for GUI access :

kubectl get secret awx-admin-password -o jsonpath="{.data.password}" | base64 --decode

Wait until All pods are Up & running and use The displayed password to Access the GUI :

http://<HOST_IP>:[NodePort]

NOTE: NodePort and GUI password are displayed during the playbook run

You can also use my Custom AWX-EE (Including community.general and other collections) :

Custom EE with PY39 : docker.io/dcmcix/py39-awx-ee:latest

Custom EE with PY38 : docker.io/dcmcix/awx-ee:latest