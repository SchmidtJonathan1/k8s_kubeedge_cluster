# k8s_kubeedge_cluster
Create Kubernetes Cluster + KubeEdge

To run the ansible playbook use:
**ansible-playbook -i inventory.ini -K -vv site.yml**

-i  = use inventory file
-K  = become root user
-vv = verbose level two (debug mode)

**Notes:**
* Add your client hostname, username and userpassword to inventory.yml or use ssl certificate for ansible.

* To set up a lab enviroment, you need two++ virutal machines (VirtualBox, VMware ...)
[VM system requirements minimum:
2 GB RAM
2 CPU (depence on the enviroment)]

* Define your kubernetes pod image in group_vars/all.yml
https://kubernetes.io/docs/concepts/cluster-administration/networking/
