At Present gluster-kubernetes only supports the ability to deploy a solution for ReadWriteMany Volumes. There is a nascent capability within Gluster to provision iSCSI targets from files within a GlusterFS volume which provides a path to supporting ReadWriteOnce (RWO) volumes provisioned from a Gluster trusted storage pool. This is a design proposal intended to be used for the gluster-kubernetes project to come to a consensus on an end-to-end system design for a RWO solution that can be built across the 3 components that currently comprise gluster-kubernetes. These components are Kubernetes, Heketi and Gluster.

The design being initially proposed is... overview.

![RWO System Design](https://github.com/wattsteve/gluster-kubernetes/blob/master/docs/design/readwriteonce.png "RWO System Design")

The changes being proposed in each component are:

External RWO Provisioner

Heketi

gk-deploy

