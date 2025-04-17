# 🚀 Kubernetes Cheat Sheet

A quick reference guide for the most commonly used `kubectl` commands and Kubernetes concepts.

---

## 🔧 Basic Commands

| Task | Command |
|------|---------|
| View cluster info | `kubectl cluster-info` |
| View all nodes | `kubectl get nodes` |
| View current context | `kubectl config current-context` |
| Switch context | `kubectl config use-context <name>` |

---

## 📦 Working with Pods

| Task | Command |
|------|---------|
| List all pods | `kubectl get pods` |
| Get pod details | `kubectl describe pod <pod-name>` |
| Create a pod (YAML) | `kubectl apply -f pod.yaml` |
| Delete a pod | `kubectl delete pod <pod-name>` |
| Logs from pod | `kubectl logs <pod-name>` |
| Execute into a pod | `kubectl exec -it <pod-name> -- /bin/bash` |

---

## 📂 Deployments & Services

| Task | Command |
|------|---------|
| List deployments | `kubectl get deployments` |
| Create deployment | `kubectl create deployment <name> --image=<image>` |
| Update deployment image | `kubectl set image deployment/<name> <container>=<new-image>` |
| Scale deployment | `kubectl scale deployment <name> --replicas=3` |
| Delete deployment | `kubectl delete deployment <name>` |

---

## 🌐 Services

| Task | Command |
|------|---------|
| List services | `kubectl get svc` |
| Expose deployment | `kubectl expose deployment <name> --type=NodePort --port=80` |

---

## 📄 YAML Apply & Delete

| Task | Command |
|------|---------|
| Apply from YAML | `kubectl apply -f <file.yaml>` |
| Delete from YAML | `kubectl delete -f <file.yaml>` |

---

## 🧪 Namespaces

| Task | Command |
|------|---------|
| List namespaces | `kubectl get ns` |
| Create namespace | `kubectl create ns <name>` |
| Use a namespace | `kubectl config set-context --current --namespace=<name>` |

---

## 🔍 Debug & Info

| Task | Command |
|------|---------|
| Describe resource | `kubectl describe <resource> <name>` |
| Events in cluster | `kubectl get events` |
| Get all resources | `kubectl get all` |

---

## 💡 Tips

- Use `-o yaml` or `-o json` to output in YAML/JSON formats.
- Add `-n <namespace>` to scope commands to a specific namespace.
- Alias suggestion: `alias k=kubectl` for faster typing.
