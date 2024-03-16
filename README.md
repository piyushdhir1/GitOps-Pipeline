# GitOps-Pipeline
# Overview Diagram
![image](https://github.com/piyushdhir1/GitOps-Pipeline/assets/82114698/b68a8b52-e1a1-413b-a31c-3d10c1b6b7dd)

# Step 01 (Initial Step)
<h3> (A) Create a minikube single node cluster.</h3>
<h3> (B) Create two namespaces for ArgoCD and applications.</h3>
<h3> (c) Use official manifests and deploy the ArgoCD Compoents in argocd namespace</h3>
<h3> (d) Create Git repo and create a Develop branch and add Readme.md file </h3>
<h3> (e) Confirm the pods are running or not in argocd namespace</h3>
<h3> (f) Port forward the Argocd service to get access the console</h3>
<h3> (g) There is secret created by ArgoCD manifests and it is in the encoded form make it decode and use as password and username as admin (as mentioned in docs) for your console login </h3>

# Step 02 (GitOps Pipeline)
<h3> (A) Dockerize 2 Application for v1.0 and v2.0 and push to the private registry</h3>
<h3> (B) In the GitHub repository add deployment manifests</h3>
<h3> (C) Open the Argocd console and click and create the application with configure and linking the GitHub repo</h3>
<h3> (D) Make the MASTER branch that will do the deployments on the cluster</h3>
<h3> (E) Use Git and create tag v1.0</h3>

# Step 03 (Canary Deployments and Rollout Object)
<h3> (A) In the Final Steps we just do the commits and all set for the deployments in the cluster.</h3>
<h3> (B) Create new tag in Github v2.0</h3>
<h3> (C) Get reference from the official docs for Canary rollout yaml and modify accordingly</h3>
<h3> (D) Replace the old manifests with Canary Deployment manifests with v2.0 docker image in v2.0</h3>
