# GitOps-Setting up the Infrastructure

Here, we set up the infrastructure end of the GitOps project. The application workflow-associated code can be found [here](https://github.com/ardhendusgit/gitops-action). We use official terraform modules and Github action modules wherever deemed necessary. Nginx Ingress Controller for the Kubernetes cluster is deployed for achieving host-based routing.

## Environment Variables

For making changes on AWS, we have to authenticate with proper credentials. We'll store these credentials securely in GitHub Secrets. The credentials used are:

- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY
- BUCKET_TF_STATE
- AWS_REGION
- EKS_CLUSTER

## Cost Optimization

Provisioning private subnets and consequently, NAT gateways is avoided to save costs. Users can uncomment and change the flag values to pursue this at will.



