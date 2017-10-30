## Kubectl in Codefresh Freestyle step
Running Kubernetes cmd in Codefresh as part of the workflow is easy.
Codefresh adding all you clusters into the workflow to be used as part of your CI/CD pipeline.
The context remain the same as it apears in Codefresh
* Use image: `codefresh/kube-helm:master`
* Add your commands
    * `kubectl config get-contexts`. Will print the cluster that we added to the workflow
    * `kubectl config use-context {cluster-name}`. The name is the same as in Account settings -> integrations -> Kubernetes
    * `kubectl get po -owide`
    * `kubectl get nodes`

# Example
* Add this repo to your account
* Change the pipeline configuration to use `codefresh.yml`.
* Build.