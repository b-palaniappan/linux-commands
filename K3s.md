## Setup K3s
* Install setup for k3s [here](https://rancher.com/docs/k3s/latest/en/installation/install-options/)
* Kubeconfig is at `/etc/rancher/k3s/k3s.yaml`
* Copy to config file to `~/.kube/config` location.
* Change Owner and Mod of config file,
```
sudo chown john:john ~/.kube/config     # change ownership of the file to user
sudo chown 400 ~/.kube/config           # only read access to the user
```
* To uninstall K3s, steps [here](https://rancher.com/docs/k3s/latest/en/installation/uninstall/)

## Install kubectl cli
* Install steps [here](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)

## Install Helm chart
* Install steps [here](https://helm.sh/docs/intro/install/#from-apt-debianubuntu)

## Install Longhorn
* Install Open-iSCSI `apt install open-iscsi` for Long Horn
* To install Long Horn, steps [here](https://rancher.com/docs/k3s/latest/en/storage/)

## Insall k9s
* `wget` latest version of linux 64 binary from github releast page [here](https://github.com/derailed/k9s/releases)
* Unzip `tar.gz` file using `tar -xvzf k9s_Linux_x86_64.tar.gz`
* Run k9s using `./k9s`
