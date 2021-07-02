
# k8s_kubeedge_cluster for Ubuntu
Create Kubernetes Cluster + KubeEdge for Ubuntu

To run the ansible playbook use:
**ansible-playbook -i inventory.ini -K -vv site.yml**

-i  = use inventory file
-K  = become root user
-vv = verbose level two (debug mode)

Check your kubernetes cluster with **kubectl get nodes**, if it list your edge node device everything works.

**Notes:**
* Add your client hostname, username and user password to inventory.yml or use ssl certificate for ansible.
Look at the cpu architecture (x64, arm or arm64)

* To set up a lab environment, you need two++ virtual machines (VirtualBox, VMware ...)
[VM system requirements minimum:
2 GB RAM
2 CPU (depending on the environment)]

* Define your kubernetes pod image in group_vars/all.yml
https://kubernetes.io/docs/concepts/cluster-administration/networking/

* Without DHCP Server, edit hosts data with IP and node name
