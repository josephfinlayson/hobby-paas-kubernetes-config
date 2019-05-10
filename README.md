What?
======

Cluster wide configuration - ingresses etc for a hobby cluster on GCP

Nice shortcuts:

Get External IPS:
`kubectl get node -o yaml | grep ExternalIP -B 1`

Shell into  pod
`kubectl exec -it POD_NAME -- /bin/sh`

Create new node pool

gcloud container node-pools create adjust-scope \
   --cluster hobby-paas --zone us-east1-c  \
   --num-nodes 3 \
   --scopes "https://www.googleapis.com/auth/ndev.clouddns.readwrite,gke-default"
   --preemptible \
   --disk-size="10GB" \
   --enable-autorepair \
   --enable-autoupgrade \
   --machine-type="f1-micro"
