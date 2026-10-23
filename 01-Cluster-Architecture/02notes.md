# 🌌 Selz's Cluster Ville

> A tiny space colony where animals, robots and aliens work together to keep Kubernetes running.

---

# 🚀 Cluster Architecture

## Mission 

Before deploying alien workloads across the galaxy, we need to understand how Cluster Ville operates.

### Topics Covered

- ✅ Kubernetes Architecture
- ✅ ETCD
- ✅ ETCD in Kubernetes
- ✅ Kube API Server
- ✅ Controller Manager
- ✅ Scheduler
- ✅ Kubelet

---

# 🪐 Welcome to Cluster Ville

Cluster Ville is a floating Ville orbiting Planet Kubernetes.

Theres main characters! Say hi to the following: 
## 🐱 The Reception Cat (Kube API Server)
## 🐿️ The Squirrel Librarian (ETCD) 
      🌙Key-value store , stores value against key 
      eg : Key : age
           Age: 67
           or like json format  simple fast lookup
           Distributed and reliable = ETCD.

 It stores things like:
Pods
Nodes
Deployments
Secrets
ConfigMaps
Namespaces
if Squirell dies thats it CLUSTER MEMORY GONE it gets alzehimer T--T
So 1- create backup :
      ETCD Backup & Restore ⭐⭐⭐
      ```
      Check backup:

    ETCDCTL_API=3 etcdctl snapshot save snapshot.db  
    ```
🐿️ "The Librarian Squirrel keeps every record in the tree library. Whenever the Reception Cat needs information about Cluster Ville, the Cat asks the Squirrel. If the library burns down and no backup exists, the entire town forgets everything." 🚀🐿️📚
## 🦉 The Scheduler 
     🌙
     🌙
     🌙

## 🤖 The  Robot Controller Manager
    🌙
    🌙
    🌙

## 🏠Worker Node 1 (VM or Physical machine)
    🌙
    🌙
    🌙

 ## 🐦‍⬛ The Kube-Proxy birdie
   🌙
   🌙
   🌙
## 🐶 The Kubelet Dog 
 🌙
 🌙
 🌙
## The Pods cute lil Alien dudes👽



---
![alt text](image.png)
![alt text](image-1.png)
![alt text](image-2.png)
![alt text](image-3.png)
![alt text](image-4.png)

