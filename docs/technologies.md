# Sandbox technology stack

* [OCI](https://opencontainers.org/) compliant container images, e.g. [Docker](https://www.docker.com/)  
* [Kubernetes](https://kubernetes.io/)
* [Helm charts](https://helm.sh/docs/topics/charts/)
* [CI/CD](https://en.wikipedia.org/wiki/CI/CD) pipeline configurations

## Secret management
The sandbox is a testing and development environment, so it has the following requirements for managing secrets:

* Use [Kubernetes secrets](https://kubernetes.io/docs/concepts/configuration/secret/)
* Don't keep secret in git repository (encrypted as well, due to rotation policy)
* Use random generated passwords, e.g. [Helm randAlphaNum method](https://helm.sh/docs/chart_template_guide/function_list/#randalphanum-randalpha-randnumeric-and-randascii)