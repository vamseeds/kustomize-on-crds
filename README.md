# kustomize-on-crds
Sample Project to report kustomize issue on crd with only additional properties

## Apply crd first
``` kubectl apply -f crd/ ```
Expected op : onlyadditionalproperties.example.com/default-oap created

customresourcedefinition.apiextensions.k8s.io/onlyadditionalproperties.example.c
om created

## Direct apply of crd document will work

```kubectl apply -f base/oap-sample.yaml```

Expected op : onlyadditionalproperties.example.com/default-oap created

## Kustomize preview will not work

``` kubectl kustomize base/ ```

Expected op : <blank>

## kustomize apply via kubectl will not work

``` kubectl apply -k base/ ```

Expected op : <blank>
