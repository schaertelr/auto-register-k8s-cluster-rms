# auto-register-k8s-cluster-rms

Execute this yaml-file on existing k3s clusters. The cluster gets created in the Rancher Management Server (RMS), and automatically registered.
When successful the cluster is ready to get managed by the RMS.


When auto-deploying k3s, add the yaml-file into /var/lib/rancher/k3s/server/manifests/ <br >
The file will get auto-executed as soon as the k3s cluster is up and running.
When successful the cluster is ready to get managed by the RMS.


IMPORTANT: provide following values in the yaml-file: <br >
  RANCHER_BEARER_TOKEN: "<your-token>"
  RANCHER_HOSTNAME: "<your-RMS-FQDN>"
  CLUSTER_NAME: "<your-cluster-name>"
