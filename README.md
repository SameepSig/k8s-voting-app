### Make sure microk8s is running:
`microk8s status --wait-ready`

If not running:
`microk8s run`

---

### Command to deploy this project:
`microk8s kubectl apply -f .`

---

### Once all the resources are created:
* Run: `microk8s kubectl get node -o wide`
* Copy the `ip address` from `internal-ip` and visit that ip in your browser. Currently I have exposed `30080` as `voting app service` and `30081` as `result app service`

---

### To delete all the created resources:

`microk8s kubectl delete -f .`