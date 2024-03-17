# GitOps-Pipeline
# Overview Diagram
![image](https://github.com/piyushdhir1/GitOps-Pipeline/assets/82114698/b68a8b52-e1a1-413b-a31c-3d10c1b6b7dd)

# Step 01 (Initial Step)
<h3> (A) Create a minikube single node cluster.</h3>
<h3> (B) Create two namespaces for ArgoCD and applications.</h3>
<h3> (C) Use official manifests and deploy the ArgoCD Compoents in argocd namespace</h3>
<h3> (D) Create Git repo and create two branches (develop and main) branch and add Readme.md file</h3>
<h3> (E) Confirm the pods are running or not in argocd namespace</h3>
<h3> (F) Port forward the Argocd service to get access the console</h3>
<h3> (G) There is secret created by ArgoCD manifests and it is in the encoded form make it decode and use as password and username as admin (as mentioned in docs) for your console login </h3>

# Step 02 (GitOps Pipeline)
<h3> (A) Dockerize 2 Application for (p5050/v1.0:1 for version 1) , (p5050/v1.0:2 for version 2) and push to the private registry</h3>
<h3> (B) In the GitHub repository add deployment manifests</h3>
<h3> (C) Open the Argocd console and click and create the application with configure and linking the GitHub repo</h3>
<h3> (D) Add main branch that will do the deployments on the cluster</h3>
<h3> (E) install rollout CRDs from official docs</h3>

# Step 03 (Canary Deployments and Rollout Object)
<h3> (A) In the Final Steps we just do the commits and all set for the deployments in the cluster.</h3>
<h3> (B) Create rollout.yaml and two services stable and canary as present in repo rollouts/ directory</h3>
<h3> (C) Get reference from the official docs for Canary rollout yaml and modify accordingly</h3>
<h3> (D) Replace the image with next version (p5050/v1.0:2) and commit</h3>
<h3> (E) I observed in the Argocd Dashboard that the 'canary' service will take the traffic from old 3 replicas and make the use of new 3 replicas as per mentioned yamls hence Canary deployment finishes</h3>



# Screenshots for the reference
![image](https://github.com/piyushdhir1/GitOps-Pipeline/assets/82114698/47ca6aaa-d27e-4e09-a6ac-7555ff4fc588)
