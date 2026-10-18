# SelzCKA-Learning

My journey towards the Certified Kubernetes Administrator (CKA) certification.

---

## Goal

I want to understand Kubernetes properly.

Not just:

- what commands to run
- what buttons to click
- how to pass an exam

Instead I want to understand:

- Why Kubernetes exists
- Why Pods exist
- Why Deployments exist
- Why networking matters
- How a cluster actually works
- How a Platform Engineer thinks

---

## Learning Philosophy

Understand the WHY before the WHAT.

Bad learning:

> Memorise command → Forget command

Good learning:

> Understand concept → Apply concept → Remember forever

---

## Learning Resources

### Killercoda

https://killercoda.com

Benefits:

- Real Linux terminal
- Real Kubernetes clusters
- Browser-based
- Free
- No installation on my machine
- CKA-focused labs

---

## Learning Path

### Week 1

Core Concepts

Topics:

- Containers
- Pods
- Nodes
- Clusters
- kubectl
- YAML

Killercoda Labs:

- Kubernetes Basics
- Pods
- Deployments

---

## Linux Commands Practice

Commands I will practise repeatedly:

### Show current directory

```bash
pwd
```

### List files

```bash
ls
```

### List hidden files

```bash
ls -la
```

### Change directory

```bash
cd
```

### View file contents

```bash
cat filename
```

### Clear terminal

```bash
clear
```

---

## Kubernetes Commands Practice

### View Nodes

```bash
kubectl get nodes
```

Question:

Why am I checking nodes?

Answer:

Nodes are the servers that run workloads inside a Kubernetes cluster.

---

### View Pods

```bash
kubectl get pods
```

Question:

What is a Pod?

Answer:

A Pod is the smallest deployable object in Kubernetes.

---

### Create a Pod

```bash
kubectl run nginx --image=nginx
```

Question:

What happened?

Answer:

Kubernetes created a Pod containing a container using the nginx image.

---

### Inspect a Pod

```bash
kubectl describe pod nginx
```

Question:

Why use this command?

Answer:

To inspect configuration, events, status and troubleshooting information.

---

### Delete a Pod

```bash
kubectl delete pod nginx
```

Question:

Why delete it?

Answer:

To understand the Pod lifecycle and clean up resources.

---

## Lab Process

For every lab:

1. Complete the lab
2. Take notes
3. Record mistakes
4. Explain the concept in my own words
5. Commit changes to GitHub

---

## Mistakes Log

I maintain a mistakes log because engineers learn through troubleshooting.

Every mistake should include:

- What happened
- Why it happened
- How I fixed it
- What I learned

---

## Git Workflow

Add changes:

```bash
git add .
```

Commit:

```bash
git commit -m "Describe work completed"
```

Push:

```bash
git push
```

---

## Personal Rule

If I cannot explain a concept in my own words, then I do not understand it yet.

Understanding comes before memorisation.