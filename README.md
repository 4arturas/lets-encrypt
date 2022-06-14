````
kubectl apply -f hello.yaml
```` 

````
kubectl apply -f welcome.yaml
````

````
minikube addons enable ingress
````

````
kubectl apply -f greeting-ingress.yaml
````

````
curl $(minikube ip)/hello
````

````
curl $(minikube ip)/welcome
````

````
kubectl create namespace cert-manager 
````

````
kubectl apply --validate=false -f https://github.com/cert-manager/cert-manager/releases/download/v1.8.0/cert-manager.yaml 
````

````
kubectl get pods -n cert-manager
````

change *spec.acme.email* in *stage-certificate.yaml*

````
kubectl apply -f stage-certificate.yaml
````

````
kubectl get clusterissuer
````

````
kubectl de
````

````
ngrok http $(minikube ip):80
````

````
kubectl delete -f greeting-ingress.yaml 
````

````
python3 /usr/local/bin/pagekite.py http://192.168.49.2 4arturas.pagekite.me
````

change *spec.tls.hosts* in *greeting-ngrok-ingress.yaml* to 4arturas.pagekite.me

````
kubectl apply -f greeting-ngrok-ingress.yaml
````

````
curl https://4arturas.pagekite.me/hello
````

````
curl $(minikube ip)/welcome
````

````
kubectl get certificate
````

wait until *READY* status will change from *False* to *True*

````
watch kubectl get certificate
````

````
kubectl describe certificate echo-tls
````

check certificate in browser by clicking the lock symbol



