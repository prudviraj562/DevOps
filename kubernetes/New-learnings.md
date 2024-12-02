1. What are annotations and labels in Kubernetes?

Annotations: Key-value pairs attached to Kubernetes objects to store **metadata** that is non-identifying and typically used by tools or systems
(e.g., monitoring or auditing). They don't affect the object's behavior or selection.

Labels: Key-value pairs used to categorize Kubernetes objects and enable selectors to **group or filter** them (e.g., for deployments or services).
They directly influence how objects are organized and managed.

Both help in metadata organization but serve distinct purposes: ---- labels for identification and annotations for descriptive metadata. ----

Examples:
============

Adding Annotations:
=====================

kubectl annotate pod <pod-name> <key1>=<value1> <key2>=<value2> --overwrite

<pod-name>: The name of the pod.
<key1>=<value1>: The annotation key-value pair.
--overwrite: Ensures that the annotation is updated if it already exists.

kubectl annotate pod my-pod environment=production team=devops --overwrite

-----------------------------------------------------------------------------------------------

Adding Labels:
================

kubectl label pod <pod-name> <key1>=<value1> <key2>=<value2> --overwrite

<pod-name>: The name of the pod.
<key1>=<value1>: The label key-value pair.
--overwrite: Ensures that the label is updated if it already exists.

kubectl label pod my-pod app=frontend tier=web --overwrite


