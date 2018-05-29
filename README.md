# Band-Aid®
aiding bands since 2017


## Kubernetes Deployment

Band-aid can be deployed on kubernetes!

First set up a kubernetes secret:

```bash

kubectl create secret generic band-aid-secret --from-file=secrets/env.json
```

Then deploy the app

```bash
kubectl apply -f deploy/manifest.yaml
kubectl apply -f deploy/service.yaml
kubectl apply -f deploy/ingress.yaml
```

Now view the app

```bash

$ kubectl get ing
NAME           HOSTS                                              ADDRESS         PORTS     AGE
main-ingress   k8snibzscience.us-south.containers.mybluemix.net   169.46.37.214   80        4d


```


Point your web browser at the hostname listed. ``k8snibzscience.us-south.containers.mybluemix.net`` in the above example.
