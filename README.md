# ocp4-etcd-backup
This project is meant to provide a sample ETCD backup solution embedded in OCP4. <br />

To apply the manifests, simply run kustomize or oc apply -k from the root of the repository: <br />
```kustomize build . | oc apply -f -``` <br />
```oc apply -k . ``` <br />

If you want to add an NFS mount just add the mount before executing the backup script in the ```ocp4-backup/etcd-bck-cronJob.yml``` file: <br />
```chroot /host  sudo -E  mount -t nfs <nfs-server-IP>:<shared-path> /home/core/backup``` <br />
and unmout it at the end: <br />
```chroot /host  sudo -E  umount /home/core/backup```

# Notes
The following articles have been used to create this Repository. <br />
**https://access.redhat.com/solutions/5843611**  <br />
**https://cloud.redhat.com/blog/ocp-disaster-recovery-part-1-how-to-create-automated-etcd-backup-in-openshift-4.x** <br />
