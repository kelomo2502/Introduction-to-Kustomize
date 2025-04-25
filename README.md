# Introduction-to-Kustomize

## Write a sample mypod.yaml file
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: mypod
spec:
  containers:
  - name: mycontainer
    image: nginx

```

This file defines a kubernetes pod named mypod with a single container running the nginx image

## Lesso 2
### Setting up the environment
Task 1: Install Kustomize
- Kustomize is a tool that allows you to customize raw, template-free YAML files for multiple purposes, essential in Kubernetes deployments.

### Detailed Steps for Linux
- Visit the Kustomize GitHub Releases Page
- Open your web browser and go to the <a href="https://github.com/kubernetes-sigs/kustomize/releases">Kustomize GitHub Releases

- Select the Appropriate Version
Choose the version that is suitable for your Linux operating system. Look for a file that ends with linux_amd64.tar.gz
- Download the tar.gz File
Click on the link for the linux_amd64.tar.gz file to download it.
- Open Terminal:
Open your terminal application.
- Navigate to the Download Directory
- Use the cd command to navigate to the directory where the downloaded file is located.
- Extract the File
Run the command: tar xzf kustomize_vX.Y.Z_linux_amd64.tar.gz, replacing X.Y.Z with the version number you downloaded.
This command will extract the Kustomize executable.

- Move Kustomize to Your PATH
Move the extracted kustomize file to a directory in your PATH for easy access. The usr/local/bin directory is a common choice.
- Run: sudo mv kustomize /usr/local/bin/
- Check Kustomize Installation:
Verify the installation by typing kustomize version in the terminal.
You should see the version of Kustomize displayed.
### Task 2: Set Up a Mini Kubernetes Cluster with Minikube
Minikube is a tool that runs a single-node Kubernetes cluster locally on your machine, ideal for learning and testing purposes.

Detailed Steps
Install Minikube:
- Visit the <a href="https://minikube.sigs.k8s.io/docs/start/">Minikube Start page.
Follow the detailed instructions provided for your specific operating system (Linux, macOS, or Windows).

### Start Minikube</strong>:
- Open your terminal.
Run the command: minikube start
This command initializes a local Kubernetes cluster.

## Start Minikube</strong>:
- Open your terminal.
Run the command: minikube start
This command initializes a local Kubernetes cluster.

## Verify Minikube Installation</strong>
Once Minikube starts, verify the cluster is up and running with the command: 
`kubectl get nodes`
This should list the nodes in your cluster, which in this case, will be a single node managed by Minikube.

### Verification Task
Run `kustomize version` in the terminal. Ensure that it displays the installed version without errors.

### Check kubectl Version</strong>:
Run `kubectl version`to ensure that kubectl is properly installed and can communicate with the Minikube cluster.

**Conclusion:**
Upon completing these tasks, you will have successfully installed Kustomize and set up a basic Kubernetes cluster using Minikube. These are essential first steps in exploring Kubernetes and learning how to manage its configurations effectively with Kustomize.