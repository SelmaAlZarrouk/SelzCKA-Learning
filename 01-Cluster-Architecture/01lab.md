# 🐿️ ETCD Lab: Save The Librarian Squirrel

---

## 📖 Story

Disaster has struck Cluster Ville.

The Librarian Squirrel lives inside the Ancient Tree Library.

Every pod, deployment, node and secret record in the entire village is stored there.

If the library catches fire 🔥...

Cluster Ville loses its memory.

My mission:

✅ Find the Squirrel

✅ Learn how to talk to him

✅ Back up his records

✅ Restore the library if disaster strikes

✅ Save the acorn stash 🥜

---

# Quest 1: Find The Librarian

## Mission

Locate where the Squirrel lives.

### Command

```bash
kubectl get pods -n kube-system
```

### Expected Discovery

```text
etcd-controlplane
```

or

```text
etcd-master
```

### Investigation

```bash
kubectl describe pod etcd-controlplane -n kube-system
```

---

## 🎮 Achievement Unlocked

+10 XP

✅ Located ETCD

+5 XP

✅ Found ETCD configuration

---

# Quest 2: Explore The Tree Library

The giant tree library contains the village's memory.

Inside are:

📚 Pods

📚 Deployments

📚 Nodes

📚 Secrets

📚 ConfigMaps

📚 Everything

If ETCD disappears...

Cluster Ville develops amnesia.

---

# Quest 3: Gain The Squirrel's Trust

The library is protected.

To speak with the Librarian Squirrel I need:

## 📜 CA Certificate

"Can I trust this library?"

```text
ca.crt
```

## 🪪 Client Certificate

"Hello, this is who I am."

```text
server.crt
```

## 🔑 Private Key

"Proof that I really am that person."

```text
server.key
```

Without these documents...

🚫 Access Denied

The Squirrel refuses to talk.

---

# Quest 4: Locate The Secret Scrolls

## Mission

Find where the certificates live.

### Command

```bash
cat /etc/kubernetes/manifests/etcd.yaml
```

### Hunt For

```text
--trusted-ca-file
--cert-file
--key-file
```

---

## 🎮 Achievement Unlocked

+15 XP

✅ Found certificate locations

---

# Quest 5: Speak To The Squirrel

Once I have the certificates, I can talk to ETCD.

Example:

```bash
ETCDCTL_API=3 etcdctl get / \
--prefix \
--keys-only \
--limit=10 \
--cacert=/etc/kubernetes/pki/etcd/ca.crt \
--cert=/etc/kubernetes/pki/etcd/server.crt \
--key=/etc/kubernetes/pki/etcd/server.key
```

---

## What Is Happening?

```text
Me:
"Hello Mr Squirrel."

Squirrel:
"Identification please."

Me:
📜 CA Certificate
🪪 Client Certificate
🔑 Private Key

Squirrel:
"Very well."
```

---

## 🎮 Achievement Unlocked

+20 XP

✅ Successfully communicated with ETCD

---

# Quest 6: The Great Backup

Oh no...

A meteor has been spotted heading directly for the tree library ☄️

Create an emergency backup.

### Command

```bash
ETCDCTL_API=3 etcdctl snapshot save /opt/backup.db
```

---

## 🎮 Achievement Unlocked

+50 XP

✅ Saved Squirrel's records

✅ Acorns secured 🥜

✅ Village protected

---

# Boss Battle: Library Fire 🔥

The tree library has been destroyed.

Restore the records.

### Command

```bash
ETCDCTL_API=3 etcdctl snapshot restore /opt/backup.db
```

---

## 🏆 CKA Skills Earned

✅ Find ETCD

✅ Read ETCD configuration

✅ Locate ETCD certificates

✅ Use etcdctl

✅ Create ETCD backup

✅ Verify ETCD backup

✅ Restore ETCD backup

---

# Selz's Exam Notes

🐿️ ETCD = Cluster Memory

🐱 API Server talks to ETCD

📜 Certificates authenticate me

💾 Snapshot = Backup

🔥 Broken ETCD = Broken Cluster

⭐ MOST IMPORTANT CKA SKILL:

Backup and Restore ETCD