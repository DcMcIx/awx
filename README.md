All Credits goes to : https://github.com/ansible/awx-operator

After The Installation :

Get NodePort :

kubectl get svc -l "app.kubernetes.io/managed-by=awx-operator" | grep -i NodePort

http://<HOST_IP>:[NodePort]

Get admin Password for GUI access :

kubectl get secret awx-admin-password -o jsonpath="{.data.password}" | base64 --decode

User The displayed password to Access the GUI