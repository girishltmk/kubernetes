# Play with kubernetes online 
https://labs.play-with-k8s.com/


Bottstrap Cluster
1. Initialize Cluster master node:
   kubeadm init --apiserver-advertise-address $(hostname -i) --pod-network-cidr 10.5.0.0/16
2. Initialize Cluster Networking
   kubectl apply -f https://raw.githubusercontent.com/cloudnativelabs/kube-router/master/daemonset/kubeadm-kuberouter.yaml
3. Create an nginx deployment
   kubectl apply -f https://raw.githubusercontent.com/kubernetes/website/master/content/en/examples/application/nginx-app.yaml
