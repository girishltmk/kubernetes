# Play with kubernetes online 
https://labs.play-with-k8s.com/


Bottstrap Cluster
1. Initialize Cluster master node:

   kubeadm init --apiserver-advertise-address $(hostname -i) --pod-network-cidr 10.5.0.0/16
2. Initialize Cluster Networking

   kubectl apply -f https://raw.githubusercontent.com/cloudnativelabs/kube-router/master/daemonset/kubeadm-kuberouter.yaml
   
 # Install K8S on Local Machine
 
 1. Install the latest MicroK8s with the following command
 
      sudo snap install microk8s --classic
      
 2. Enable necessary addons from the list above. The command below enables dashboard and dns addons.
 
     sudo microk8s.status
     sudo microk8s.enable dashboard dns
     
 3. Access kubernetes
 
      sudo microk8s.kubectl get all --all-namespaces
      sudo microk8s.kubectl cluster-info
      
      
      

