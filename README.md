In some cases CRDs in Helm charts will contain the `status` object.  The 'stats' object should not be defined and creates an issue when importing CRDs with it into Anthos Configuration Management.  This repo is an example of how to remove the `status` object before applying it to Anthos Configuration managment

````
nomos hydrate --source-format=unstructured --output=.hydrated --no-api-server-check
````
