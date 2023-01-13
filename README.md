# Provision of EKS Cluster

## Configuration

The configuration is organized across multiple files:

> **terraform.tf** sets the Terraform version to at least 1.3. It also sets versions for the providers used by the configuration.

> **variables.tf** contains a region variable that controls where to create the EKS cluster

> **vpc.tf** provisions a VPC, subnets, and availability zones using the AWS VPC Module. The module creates a new VPC for this tutorial so it doesn't impact your existing cloud environment and resources.

> **eks-cluster.tf** uses the AWS EKS Module to provision an EKS Cluster and other required resources, including Auto Scaling Groups, Security Groups, IAM Roles, and IAM Policies.  The eks_managed_node_groups parameter will create three nodes across two node groups.

> **outputs.tf** defines the output values for this configuration.