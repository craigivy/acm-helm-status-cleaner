# Anthos Configuration Mananment using Helm
## Removing unwanted elements from CRDs with Kustomize
In some cases CRDs in Helm charts will contain the `status` element.  The `stats` element should not be defined and creates an issue when importing CRDs with it into Anthos Configuration Management.  This repo is an example of how to remove the `status` object before applying it to Anthos Configuration managment. This builds off the Google Cloud [example](https://cloud.google.com/anthos-config-management/docs/tutorials/config-sync-helm#gcloud_2)

Validating the process works
````
nomos hydrate --source-format=unstructured --output=.hydrated --no-api-server-check
````
