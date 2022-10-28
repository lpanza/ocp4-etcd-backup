# ocp4-etcd-backup
This project is meant to provide a sample ETCD backup solution embedded in OCP4.

If you want to add an NFS mount just add the mount before executing the script:
```chroot /host  sudo -E  mount -t nfs <nfs-server-IP>:<shared-path> /home/core/backup```
and unmout it at the end
```chroot /host  sudo -E  umount /home/core/backup```

