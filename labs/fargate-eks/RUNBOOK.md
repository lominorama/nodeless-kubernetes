### 0 min mark
* (nacho) `SLIDES` Introduction to virtual kubelet and the lab

### 10 min mark
* (roi) `TALK` We have now an EKS cluster
* (roi) `CODE` Show very quickly the terraform for the EKS cluster

### 12 min mark
* (roi) `TALK` How anyone ever used EKS?
  * It is a very bare Kubernetes instalation, with a very limited set of functionality: control plane,  networking and service discovery. Let's check It.
* (roi) `COMMAND` Get the cluster credentials with awscli
* (roi) `COMMAND` Describe pods
* (roi) `QUESTION` Why we only have the coredns pod?

### 17 min mark
* (nacho) `SLIDES` Add an ECS cluster
* (roi) `COMMAND` Deploy the ECS cluster
* (roi) `CODE` Briefly show code

### 20 min mark
* (nacho) `SLIDES` Add a virtual-kubelet ECS service
* (roi) `COMMAND` Create the image
* (roi) `COMMAND` Deploy the ECS service for virtual-kubelet
* (roi) `CODE` Show terraform code and Dockerfile
* (roi) `QUESTION` Will virtual-kubelet be able to register itself as a Kubernetes "node"?
* (roi) `COMMAND` Deploy the aws-iam-auth-config.yaml and recycle virtual-kubelet ECS task
* (roi) `COMMAND` Show `kubectl get nodes`

### 30 min mark
* (nacho) `SLIDES` Create an nginx demo Deployment
* (roi) `COMMAND` Deploy the nginx manifest
* (roi) `BROWSER` Get the IP of one of the pods from the ECS console and test the Deployment
* (roi) `QUESTION` How do we create some kind of load balancing to distribute requests to the 3 nginx pods?

### 40 min mark
* (nacho) `SLIDES` Add an ingress controller (traefik)
* (roi) `COMMAND` Deploy the k8s manifest for traefik
* (roi) `COMMAND` Deploy the traefik ECS service and the ALB
* (roi) `BROWSER` Show the traefik dashboard
* (roi) `BROWSER` Get the ALB endpoint and test it in the browser