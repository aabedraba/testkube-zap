# Testkube + ZAP Example 

This example shows how to use ZAP to scan for OWASP security breaches in Kubernetes's apps using[Testkube](https://testkube.io), an Open Source testing orchestration tool for Kubernetes.  

## Run the example

1. Install [Testkube](https://docs.testkube.io/getting-started) in your Kubernetes cluster.

2. Clone this repository and navigate to the example directory.

3. Create the test in Testkube:

```sh
testkube create test --name zap-example --type zap/api --file zak-tk.yaml --copy-files zap-tk-api.conf:zap-tk-api.conf
```

4. Run the test: 

```sh 
testkube run test --name zap-example
```