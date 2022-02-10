---
title: "Clustering"
weight: 60
geekdocCollapseSection: true
---

TrueCommand 2.1, in conjunction with TrueNAS SCALE, can create clustered volumes that span across multiple volumes. 

There are five TrueNAS volume types:

+ Replicated - Use Replicated for better reliability and data redundancy, and to overcome the risk of data loss in a distributed volume. It creates copies of files across multiple bricks in the volume. Use replicated volumes in environments where high-availability and high-reliability are critical. 
+ Distributed - Use Distributed where scalable storage and redundancy is either not important, or is provided by other hardware or software layers. A distributed volume easily and cheaply scales the volume size but can suffer significant data loss during a disk or server failure because directory contents are randomly spread across the bricks in the volume.
+ Dispersed - Use Dispersed to disperse data across the bricks. Dispersed volumes allow a configurable level of reliability with minimal wasted storage space. In dispersed volume data is broken into fragments, expanded and encoded with redundant data pieces and stored across a set of different bricks.
+ Distributed Replicated - Use Distributed Replicated to distribute data across replicated sets of brickes. This volume creates distributed copies of multiple bricks in the volume. Use distributed replicated volumes in environments where high-availability and high-reliability are critical.
+ Distributed Dispersed - Use Distributed Dispersed to distripute and disperse data across a set of different bricks. Data is distributed and broken into fragments, expanded and encoded with redundant data pieces and stored across a set of different bricks. This feature is not implemented yet.


{{< hint danger >}}
Cluster volume management is a BETA feature in TrueCommand 2.0 and 2.1. 
Before using such features, back up all your data. 
Do not rely on this for critical data.
{{< /hint >}}

{{< hint warning >}}
TrueNAS does not support distributed dispersed volumes at this time.

The cluster feature uses reverse DNS lookup. A valid reverse lookup is required.
{{< /hint >}} 


![ClusterVolumeDashboard](/images/TrueCommand/2.1/ClusterVolumeDashboard.png "ClusterVolumeDashboard")
