https://cloud.google.com/sdk/docs/install#deb

What is the gcloud CLI?
The Google Cloud CLI is a set of tools to create and manage Google Cloud resources. You can use these tools to perform many common platform tasks from the command line or through scripts and other automation.

For example, you can use the gcloud CLI to create and manage the following:

Compute Engine virtual machine instances and other resources
Cloud SQL instances
Google Kubernetes Engine clusters
Dataproc clusters and jobs
Cloud DNS managed zones and record sets
Cloud Deployment Manager deployments


## Install the gcloud CLI 

Before you begin
Before you install the gcloud CLI, make sure that your operating system meets the following requirements:

 - It is an Ubuntu release that hasn't reached [end-of-life](https://wiki.ubuntu.com/Releases) or a Debian stable release that hasn't reached [end-of-life](https://wiki.debian.org/DebianReleases)
It has recently updated its packages:

`sudo apt-get update
`

 - It has [apt-transport-https](https://packages.debian.org/bullseye/apt-transport-https) and curl installed
`
sudo apt-get install apt-transport-https ca-certificates gnupg curl


1.   Installation
Import the Google Cloud public key.
- For newer distributions (Debian 9+ or Ubuntu 18.04+) run the following command:
`
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /usr/share/keyrings/cloud.google.gpg
`

- For older distributions, run the following command:
`
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key --keyring /usr/share/keyrings/cloud.google.gpg add `

- If your distribution's apt-key command doesn't support the --keyring argument, run the following command:

curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

If you can't get latest updates due to an expired key, [obtain the latest apt-get.gpg key file](https://cloud.google.com/compute/docs/troubleshooting/known-issues#keyexpired).

2.  Add the gcloud CLI distribution URI as a package source

### For newer distributions (Debian 9+ or Ubuntu 18.04+), run the following command:
```
echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
```
###  For older distributions, run the following command:
```
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key --keyring /usr/share/keyrings/cloud.google.gpg add 

```


**Note: Make sure you don't have duplicate entries for the cloud-sdk repo in /etc/apt/sources.list.d/google-cloud-sdk.list.**


3.  Update and install the gcloud CLI : 

```
sudo apt-get update && sudo apt-get install google-cloud-cli
```

For additional apt-get options, such as disabling prompts or dry runs, refer to the [apt-get man pages](https://linux.die.net/man/8/apt-get).
Docker Tip: If installing the gcloud CLI inside a Docker image, use a single RUN step instead:
```
RUN echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | tee -a /etc/apt/sources.list.d/google-cloud-sdk.list && curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /usr/share/keyrings/cloud.google.gpg && apt-get update -y && apt-get install google-cloud-sdk -y    
```

For older base images that do not support the gpg --dearmor command:
```

RUN echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | tee -a /etc/apt/sources.list.d/google-cloud-sdk.list && curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key --keyring /usr/share/keyrings/cloud.google.gpg  add - && apt-get update -y && apt-get install google-cloud-cli -y
      

``
4.   (Optional) Install any of the following [additional components](https://cloud.google.com/sdk/docs/components#additional_components):

google-cloud-cli
google-cloud-cli-anthos-auth
google-cloud-cli-app-engine-go
google-cloud-cli-app-engine-grpc
google-cloud-cli-app-engine-java
google-cloud-cli-app-engine-python
google-cloud-cli-app-engine-python-extras
google-cloud-cli-bigtable-emulator
google-cloud-cli-cbt
google-cloud-cli-cloud-build-local
google-cloud-cli-cloud-run-proxy
google-cloud-cli-config-connector
google-cloud-cli-datastore-emulator
google-cloud-cli-firestore-emulator
google-cloud-cli-gke-gcloud-auth-plugin
google-cloud-cli-kpt
google-cloud-cli-kubectl-oidc
google-cloud-cli-local-extract
google-cloud-cli-minikube
google-cloud-cli-nomos
google-cloud-cli-pubsub-emulator
google-cloud-cli-skaffold
google-cloud-cli-spanner-emulator
google-cloud-cli-terraform-validator
google-cloud-cli-tests
kubectl



5. Run [gcloud init](https://cloud.google.com/sdk/gcloud/reference/init) to get started

``
gcloud init
``


## Downgrading gcloud CLI versions

To revert to a specific version of the gcloud CLI, where VERSION is of the form 123.0.0, run the following command:

``
sudo apt-get update && sudo apt-get install google-cloud-cli=123.0.0-0
``





























