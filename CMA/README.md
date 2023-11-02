### Install Custom Metric Autoscaler using Operator Framework via CLI:

#### Steps 1
- Check out this repo and cd it to CMA directory

#### Step 2
- Verify if you have OC cli installed with Kustomize. Make sure you are logged in with a user who has 'cluster-admin' privileges before running the below commands.

```bash 
oc - version
```
![[Pasted image 20231102082705.png]]
#### Step 3
Here we will apply the kustomization that we have created for the Dev environment. You can apply directly from the `base` directory or from the `overlays/dev` directory.

```bash 
oc apply -k overlays/dev
```
#### Step 4
If the above step does not indicate any errors then go ahead and verify if the CMA operator is installed and ready via console or on CLI.

For CLI:
```bash
oc get pods -n openshift-keda
```
![[Pasted image 20231102082948.png]]

For Console look under Operators tab and then Installed Operators on left pane. 
