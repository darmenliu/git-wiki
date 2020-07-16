# Kubernetes commands

```
kubectl api-versions
curl http://localhost:10252/metrics

命令自动补全：
apt-get install bash-completion
source /usr/share/bash-completion/bash_completion
echo 'source <(kubectl completion bash)' >>~/.bashrc
kubectl completion bash >/etc/bash_completion.d/kubectl

access your Pod via the network
kubectl port-forward <pod-name> 8080:80
kubectl top nodes




kubectl.exe cluster-info dump
kubectl get pods --all-namespaces 
kubectl logs kubernetes-dashboard-5bff5f8fb8-r7l4x --namespace=kube-system
kubectl get deployment
kubectl describe deployment webapp1

kubectl -n kube-system delete $(kubectl -n kube-system get pod -o name | grep dashboard)

kubectl get deployments

kubectl delete pod myubuntu-554c689fff-9z84j
kubectl get pods
kubectl.exe describe pod first-deployment-5759cbd449-ndmlx
kubectl.exe expose deployment first-deployment --type=NodePort
kubectl.exe get services
kubectl.exe describe service first-deployment
minikube.exe service --url=true first-deployment

```


