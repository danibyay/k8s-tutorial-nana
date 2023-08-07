# k8s-tutorial-nana
following tutorial of Techworld with Nana


Deploy a simple cluster with two deployments
- mongo
- sample web app with nodejs

This files were ran and tested on minikube on macOS

after doing kubectl apply -f <filename> to all the four files, be sure to run this command to be able to access the web app in your browser

> minikube service --url name_of_service

and to get the name of the service run

> kubectl get svc

example

> minikube service --url webapp-service

Make sure that the service you want to access in the browser has the nodeport type.

In my case the url was *'http://127.0.0.1:50555'*

---
Other minikube commands 

        minikube start

        minikube start --driver=docker

        minikube dashboard

        kubectl get

        kubectl delete 

        minikube ip


192.168.49.2:30100

In theory I should be able to access it via the minikube IP and the nodeport 30100 configured in webapp.yaml, but what worked was 127.0.0.1:50555