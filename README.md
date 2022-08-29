helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
helm search repo app -l
ll
helm repo add nfs-subdir-external-provisioner https://kubernetes-sigs.github.io/nfs-subdir-external-provisioner
helm repo update
helm install nfs-subdir-external-provisioner nfs-subdir-external-provisioner/nfs-subdir-external-provisioner     --set nfs.server=192.168.37.105 --set nfs.path=/mnt/IT-Academy/nfs-data/sa2-21-22/
helm install my-release --set global.storageClass=nfs-client,wordpressUsername=migel,wordpressPassword=alfa32,mariadb.auth.rootPassword=alfa bitnami/wordpress
nano wp_ingress.yaml
kubectl apply -f wp_ingress.yaml
sudo nano /etc/hosts

