What?
======

Cluster wide configuration - ingresses etc for a hobby cluster on GCP

Nice shortcuts:

Get External IPS:
`kubectl get node -o yaml | grep ExternalIP -B 1`

Shell into pod
`kubectl exec -it POD_NAME -- /bin/sh`
