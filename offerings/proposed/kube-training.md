This is me thinking out loud about a curriculum for teaching the Kube stack to Garage consultants. The plan would be to publish it on the Garage Method website and eventually make it available to customers as well. -- Bobby Woolf

# Basics

|**Stage**|**Concepts**|**IKS Lab**|**ICP Lab**|**startkit**|
| ----- | ----- | ----- | ----- | ----- |
|1|n/a|[Scalable web application on Kubernetes](https://cloud.ibm.com/docs/tutorials?topic=solution-tutorials-scalable-webapp-kubernetes)|[Cloud-native applications in IBM Cloud Private](https://www.ibm.com/cloud/garage/content/course/cloud-native-applications-in-ibm-cloud-private)||
|2|Docker ([Containers and Docker](https://www.ibm.com/cloud/garage/content/course/containers-and-docker))<td colspan=2>Docker tasks on laptop: pull, build, push, etc.
|3|Kube cluster ([Kubernetes 101](https://www.ibm.com/cloud/garage/content/course/kubernetes-101))|Create an IKS cluster|Create an ICP cluster|[iks-cluster.template.tf](https://github.ibm.com/garage-catalyst/iteration-zero-terraform/blob/master/src/templates/ibmcloud/iks-cluster.template.tf)|
|4|Deploying an app: Pod, Deployment, Service ([Kubernetes 101](https://www.ibm.com/cloud/garage/content/course/kubernetes-101))<td colspan=2>Deploy a simple monolith
|5|Helm: Chart, Template ([Get started with Helm](https://www.ibm.com/cloud/garage/content/course/helm-fundamentals))|||[helm-provider.template.tf](https://github.ibm.com/garage-catalyst/iteration-zero-terraform/blob/master/src/templates/helm/helm-provider.template.tf), [tiller.template.tf](https://github.ibm.com/garage-catalyst/iteration-zero-terraform/blob/master/src/templates/kubernetes/tiller.template.tf)|
|6|Bind a backend service: Secret|`ibmcloud ks cluster-service-bind`<br/>Tutorial: Creating Kubernetes clusters: [Lesson 4: Adding a service to your cluster](https://cloud.ibm.com/docs/containers?topic=containers-cs_cluster_tutorial#cs_cluster_tutorial_lesson4)|TBD|
|7|Externalize config: ConfigMap|||

# User Management

|**Stage**|**Concepts**|**IKS Lab**|**ICP Lab**|**startkit**|
| ----- | ----- | ----- | ----- | ----- |
|1|Kubernetes RBAC|||
|2|Users and resources: IAM|||[resource-group.template.tf](https://github.ibm.com/garage-catalyst/iteration-zero-terraform/blob/master/src/templates/ibmcloud/resource-group.template.tf), [user-policies.template.tf](https://github.ibm.com/garage-catalyst/iteration-zero-terraform/blob/master/src/templates/ibmcloud/user-policies.template.tf)|
|3|Organizing teams and apps: IAM|[Best practices for organizing users, teams, applications](https://cloud.ibm.com/docs/tutorials?topic=solution-tutorials-users-teams-applications)||
|4|User authentication: App ID|Apply end to end security to a cloud application: [Authenticate users](https://cloud.ibm.com/docs/tutorials?topic=solution-tutorials-cloud-e2e-security#authenticate-users)||
  
# DevOps

|**Stage**|**Concepts**|**IKS Lab**|**ICP Lab**|**startkit**|
| ----- | ----- | ----- | ----- | ----- |
|1|DevOps: Build pipeline|[Continuous Deployment to Kubernetes](https://cloud.ibm.com/docs/tutorials?topic=solution-tutorials-continuous-deployment-to-kubernetes)|A Jinkins tutorial that can be used in both IKS and ICP|
|2|Continious integration||||
|3|Continious delivery||||
|4|Health management: Readiness, Liveness||||
|5|Monitoring: [Explore Cloud Service Management and Operations](https://www.ibm.com/cloud/garage/content/course/explore-csmo)||||
|6|Logging||||

# Networking

|**Stage**|**Concepts**|**IKS Lab**|**ICP Lab**|**startkit**|
| ----- | ----- | ----- | ----- | ----- |
|1|Client access: Ingress Controller|Scalable web application on Kubernetes: [Use the IBM-provided domain for your cluster](https://cloud.ibm.com/docs/tutorials?topic=solution-tutorials-scalable-webapp-kubernetes#ibm_domain)||
|2|Custom domain: Ingress host|Scalable web application on Kubernetes: [Use your own custom domain](https://cloud.ibm.com/docs/tutorials?topic=solution-tutorials-scalable-webapp-kubernetes#custom_domain)||
|3|On-prem: strongSwan VPN|||
|4|Network configuration: Network Policy|||

# Resiliancy

|**Stage**|**Concepts**|**IKS Lab**|**ICP Lab**|**startkit**|
| ----- | ----- | ----- | ----- | ----- |
|1|Autoscaling, Resource requests and limits|||| 
|2|Multizone clusters||n/a||
|3|Multi-region clusters: Cloud Internet Services|[Resilient and secure multi-region Kubernetes clusters with Cloud Internet Services](https://cloud.ibm.com/docs/tutorials?topic=solution-tutorials-multi-region-k8s-cis)|n/a||
|4|Resiliancy in ICP|n/a|[Deploy a resilient application with Kubernetes](https://www.ibm.com/cloud/garage/content/course/kubernetes-intermediate)||
|5|[IBM Cloud Private resilience](https://www.ibm.com/cloud/garage/content/course/ibm-cloud-private-resilience)|n/a|||

# Service Mesh

|**Stage**|**Concepts**|**IKS Lab**|**ICP Lab**|**startkit**|
| ----- | ----- | ----- | ----- | ----- |
|1|Microservices deployment: Istio intelligent routing|||
|2|Microservices resiliency: Istio resiliancy and vistualization|||
|3|Microservcices security: Istio security|||

# Getting started with ICP

|**Stage**|**Concepts**|**IKS Lab**|**ICP Lab**|**startkit**|
| ----- | ----- | ----- | ----- | ----- |
|1|ICP architecture: [Introduction to IBM Cloud Private](https://www.ibm.com/cloud/garage/content/course/ibm-cloud-private-introduction)|n/a|[IBM Cloud Private Trial](https://bluedemos.com/show/1484)||
|2|ICP installation: [IBM Cloud Private installation and configuration](https://www.ibm.com/cloud/garage/content/course/ibm-cloud-private-installation)|n/a|||
|3|ICP storage: [IBM Cloud Private essentials: Persistent storage](https://www.ibm.com/cloud/garage/content/course/ibm-cloud-private-persistent-storage)||||
|4|ICP networking: [Networking and IBM Cloud Private](https://www.ibm.com/cloud/garage/content/course/ibm-cloud-private-networking)|||
|5|ICP security: [Explore security in IBM Cloud Private](https://www.ibm.com/cloud/garage/content/course/ibm-cloud-private-security)|||

More to be added.
