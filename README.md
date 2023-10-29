# nfs-auto-provisioner-for-openshift
## What does nfs-auto-provisioner-for-openshift do?
It does just that! This script enables the following under OpenShift:
1) it sets up your OpenShift cluster to provide NFS provisioning with subdirectories
2) it sets up a storage class for consumption
3) it provides a mechanism to test the logic above

And - it provides mechanisms to progress and rollback both the autoprovisioner AND the test

Become a cluster adming and then, before running, be sure to at a minimum, configure the top two variables:

NFS_SERVER=<your-nfs-server-hostname-or-ip-address   
NFS_PATH=/your/nfs/server/shared/path   

This is simply a bash automation of the process above, based on:  
https://github.com/kubernetes-sigs/nfs-subdir-external-provisioner#manually
