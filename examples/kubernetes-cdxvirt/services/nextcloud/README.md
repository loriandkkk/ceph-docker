# Nextcloud

- based on wonderfall/nextcloud:10.0 & mysql

develop/nextcloud	10.0	6aeaa1562b36	11 days ago	221.2 MB

## init Nextcloud rbd image

- `rbd create nextcloud-app --size 2048`
- `rbd create nextcloud-config --size 2048`
- `rbd create nextcloud-data --size 2048`
- `rbd create nextcloud-db --size 2048`
- `docker build -t develop/nextcloud:10.0 .`
- Change PV's yaml ceph mon IP

## Create Nextcloud

- `kubectl create -f pv/nextcloud-app-pv.yaml  -f pv/nextcloud-config-pv.yaml -f pv/nextcloud-data-pv.yaml -f pv/nextcloud-db-pv.yaml -f nextcloud-db.yaml -f nextcloud.yaml`
