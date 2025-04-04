### csi-driver-nfs

Create NFS CSI stoarge Class - Connecting an NFS server, such as a common Linux server, to OpenShift can be a convenient way to provide storage for multi-pod (ReadWriteMany/RWX) Persistent Volumes. Fancy NFS servers, like NetApp or Dell/EMC Isilon, have their own Container Storage Interface (CSI) drivers and shouldn't use the csi-driver-nfs described in this document. Using the appropriate CSI driver for your storage provides additional features like efficient snapshots and clones. The goal of this document is to describe how to install the csi-driver-nfs provisioner onto OpenShift. The procedure can be performed using the Web Console, but I'll document the Helm/command-line method here because it's easier to copy and paste.
* Please note: The ServiceAccounts created by the official Helm chart require additional permissions in order to overcome OpenShift's default security policy and run the Pods.

https://hackmd.io/@johnsimcall/BJeW2Y5mT#Create-a-VolumeSnapshotClass\

- Install the Helm CLI tool
- Add the Helm repo and list available charts
- Install a chart release
- Grant additional permissions to the ServiceAccounts
- Create a StorageClass
- Create a VolumeSnapshotClass
