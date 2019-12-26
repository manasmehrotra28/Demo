# Demo
We have to deploy Jenkins app on Kubernetes cluster, create a deployment for this Jenkins app on master node (file given above).

    $ sudo kubectl create -f <deployemnt_name.yaml>

now check our deployments by this command,

    $ sudo kubectl get deployments

and status of pods with this command,

    $ sudo kubectl get pods

Our deployment is successful, now expose this pod to outside world for accessing the app we use service as a NodePort.

    $ sudo kubectl expose deployment <deployment_name> --type=NodePort

Now, our deployment are exposed for accessing this check the svc to know the ports and ips.

    $ sudo kubectl describe pod <pod_name>

Then, run our app on port given in NodePort with localhost. (localhost:30000-32767)
