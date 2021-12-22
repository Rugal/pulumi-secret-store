# How to generate this code

1. find CRD file in [github](https://github.com/kubernetes-sigs/secrets-store-csi-driver/tree/main/charts/secrets-store-csi-driver/crds)
1. use `crd2pulumi` to generate target code
1. Replace `| undefined>` with `>`
    ```shell
    sed -i 's/ | undefined>/>/g' src/*
    ```
1. Then you can build the package and deploy it to npm
   ```shell
   yarn build && yarn deploy
   ```