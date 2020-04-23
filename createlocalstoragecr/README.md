eval $(ssh-agent)

ssh-add /root/ocp43/ocp4_id_rsa

specify ocs nodes in hosts

specify ocs devices in DiskInfo.yml

If using the following taint for ocs nodes:
node.ocs.openshift.io/storage=true:NoSchedule
Then set the add_toleration var to true in DiskInfo.yml.  If not, then false. 

ansible-playbook DiskInfo.yml

look for output file "ocs_local_storage_config.yaml"
