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

https://7b11-84-15-180-123.eu.ngrok.io/hello
https://7b11-84-15-180-123.eu.ngrok.io/welcome

change *spec.rules.host* in *greeting-ngrok-ingress.yaml*

````
kubectl delete -f greeting-ingress.yaml 
````

````
kubectl get certificate
````

````
kubectl describe certificate echo-tls
````



