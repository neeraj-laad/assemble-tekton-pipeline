This is a sample tekton pipeline that can take a base application as a docker hub image and overlay it on top of an user application (http endpoint) and then building and pushing het assembled application image back to  dockerhub.

# Prerequisites

1. Kubernetes cluster (I used Docker Desktop on Mac)
1. Tekton pipelines (0.1.0) (released with Knative 0.4.0) 
1. Dockerhub account
1. Github account

# Usage

1. Edit the yaml files and replace `<INSERT>` with your account details (github, dockerhub), secret (dockerhub) etc. 
2. Apply all the yaml files to create the resources, secrets, tasks and pipeline.

`kubectl apply -f .`

# Monitor build pipeline:

`kubectl get pods -w`

# See build pipeline logs:

`kubectl logs <pod-name> --all-containers`
