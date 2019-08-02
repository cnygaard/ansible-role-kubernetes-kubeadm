# ansible-role-kubernetes-kubeadm
Ansible Role that deploys a Kubernetes cluster to localhost via Kubeadm

### Ansible Roles used in this playbook ###
    - role: kubernetes-reset
      This role does a full kubernetes kubeadm cluster reset when Ansible variable kubernetes_reset: true

    - role: geerlingguy.docker
      Ansible galaxy role docker written by Jeff Gerling.

    - role: geerlingguy.kubernetes
      Ansible galaxy role Kubernetes written by Jeff Gerling. Does Kubernetes deploy via kubeadm

    - role: andrewrothstein.kubernetes-helm
      Ansible galaxy role kubernetes-helm written by Andrew Rothstein that installs Helm

    - role: ansible-role-kubectl-krew
      Ansible role that install kubectl krew plugin which can be used to install Nginx-ingress controller

    - role: helm
      Ansible role that does Helm init

    - role: kubernetes-metal-lb
      Ansible role that applies bare metal Kubernetes Load balancer for use with Bare metal Kubernetes installations.

### Variables

Ansible host file
hosts, currently specifies localhost. 

If you add more host you need to specify Ansible variable if the Kubernetes node is master or  node
kubernetes_role: maste
or
ubernetess_role: node

kubernetes_reset: true/false If you should do a full Cluster reset.


