# Role `k8s-cni-weave`

This role initializes pod networking using [Weave Net](https://www.weave.works/docs/net/latest/overview/). It must be executed once - preferably on the first master after the cluster was created.

See also the big [picture](../../docs/roles.md).

## Configuration

This role does not require any configuration.

## Usage

The following play install Weave Net in the cluster.

```ansible
- name: Initialize networking
  hosts: first_controller
  roles:
    - role: k8s-cni-weave
```
