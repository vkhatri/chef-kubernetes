# 1.11.5 (19.07.2018)
- podman upgraded to 0.7.2
- Kubernetes: 1.11.1
- Etcd systemd unit default name set to `etcd` instead of `etcd-#{node['name']}`

# 1.11.4 (13.07.2018)
- CoreDNS: 1.2.0
- kube-proxy: explicitly set cluster-cidr
- kube-proxy: simplify proxy-mode configuration
- Make kubernetes services network route ipvs compatible
- Packages: install `ipvsadm` and `ipset` for IPVS proxy mode
- kube-proxy: split attributes to global and ipvs-related
- sdn canal: calico updated to 3.1

# 1.11.3 (11.07.2018)
- CNI plugins: bump to 0.7.1
- podman: 0.7.1
- cri-o: 1.11.1

# 1.11.2 (07.07.2018)
- Kubelet: add ability to use custom runtimes
- `kubeletconfig`: check for `RotateKubeletServerCertificate` feature gate before enabling server certificates autorotation
- Docker moved to separate recipe
- install CRIO and corresponding binaries
- Buildah installation recipe
- Explicitly install aufs-tools if cri-o uses aufs as storage
- `kubeletconfig`: explicitly set cgroup driver

# 1.11.1 (28.06.2018)
- Kubernetes: 1.11.0
- Feature gates: remove already enabled by default `MountPropagation` and `VolumeScheduling`
- `recipes/proxy`: typo fix in `LimitNOFILE` systemd-unit instruction
- `kubeletconfig`: fix unexpected camelcase in keys
- `kubeletconfig`: explicitly add TLS-settings

# 1.11.0 (27.06.2018)
- Delete kubernetes dashboard from cookbook
- Kubernetes: 1.11.0-rc.3
- KubeDNS: 1.14.10
- Get rid of upstart (and ubuntu-trusty) support

# 1.10.6 (21.06.2018)
- Return `create` action for etcd recipe
- Add checksum validation for etcd tarball

# 1.10.5 (21.06.2018)
- Kubernetes updated to 1.10.5

# 1.10.4 (21.06.2018)
- [breaking] Upgrade docker from `docker-engine-1.12` to `docker-ce-17.03`
- Etcd updated to 3.3.8

# 1.10.3 (20.06.2018)
- CoreDNS update to [1.1.4](https://github.com/coredns/coredns/releases/tag/v1.1.4)

# 1.10.2 (13.06.2018)
- Add ReadOnlyPort for kubelet. Need for heapster auth.

# 1.10.1 (06.06.2018)
- Etcd updated to [3.3.7](https://github.com/coreos/etcd/blob/master/CHANGELOG-3.3.md#v337-2018-06-06)
- Kubernetes updated to [1.10.4](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG-1.10.md#changelog-since-v1103)

# 1.10.0 (31.05.2018)
- Update versioning procedure. From now on major and minor parts coincedes with Kubernetes major and minor, and patch version reflects the current release number
- Kubernetes updated to 1.10.3
- CoreDNS updated to 1.1.3
- Etcd updated to 3.3.5

# 0.1.3 (15.04.2018)
- Upgrade etcd cookbook dependency from 4.1 to 5.5
- Add chef-client 14 support

# 0.1.2 (14.04.2018)
- Weave: 2.3.0
- Weave: split `--status-addr` into separate `--status-addr` and `--metrics-addr` args
- Weave: make status port and metrics port as attributes
- Etcd: 3.3.3

# 0.1.1 (14.04.2018)
- Kubernetes 1.10.1

# 0.1.0 (05.04.2018)
- Use --config for kubelet
- Change featureGates struct from string to hash
- Update helpers.rb for backward compatibility with service options
- Reanimate inspec with testkitchen.
- Fix docker built-in variables into recipe
- Move kube-proxy config args from recipe to k8s_proxy.rb
- Add sort for master nodes in haproxy config
- Bump cniVersion from 0.3.0 to 0.3.1
- Add haproxy reload by default

# 0.0.4 (03.04.2018)
- Bump to 1.10.0 kubernetes version
- Change packages array to hash
- Move cni plugins symlinks to attributes for enable/disable actions
- Move kubelet args to attributes/kubelet.rb from recipe
- Move apiserver args to attributes/k8s_apiserver.rb from recipe
- Move scheduler args to attributes/scheduler.rb from recipe
- Move controller_manager args to attributes/k8s_controller.rb from recipe

# 0.0.3 (11.03.2018)
- Add custom docker installation. Default `true`. But if you have another docker
  installation you can skip built-in.
- Move packages array from `packages.rb` to default attrs file
- Update README.md for new users.

# 0.0.2 (29.06.2016)

- Bunch of runit services replaced by manifests
- Kubernetes updated to 1.2.5
- Node down detection moved from a 5m40s to 46s (via https://fatalfailure.wordpress.com/2016/06/10/improving-kubernetes-reliability-quicker-detection-of-a-node-down/)
- Weave scope to visualize container network

# 0.0.1

Initial release of kubernetes
