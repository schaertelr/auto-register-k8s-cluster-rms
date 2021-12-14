# auto-register-k8s-cluster-rms

This yaml-file helps to avoid manually adding k3s clusters into the Rancher Management Server via the web-gui. <br >
The version of RMS is 2.6.2, k3s is v1.21.7+k3s1.

Execute this yaml-file on existing k3s clusters. The cluster gets created in the RMS and automatically registered. <br >
When successful the cluster gets active and ready to get managed by the RMS.


When auto-deploying k3s, add the yaml-file into /var/lib/rancher/k3s/server/manifests/ <br >
Don't forget to chmod 600 the yaml-file for security reasons. <br >
The file will get auto-executed as soon as the k3s cluster is up and running.
When successful the cluster gets active and ready to get managed by the RMS.


IMPORTANT: provide your values of the following variables in the yaml-file: <br >
&emsp; RANCHER_BEARER_TOKEN: "your-token" <br >
&emsp; RANCHER_HOSTNAME: "your-RMS-FQDN" <br >
&emsp; CLUSTER_NAME: "whatever-cluster-name"
