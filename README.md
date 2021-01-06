# 

## Prerequisite

```
go version
go version go1.15.5 darwin/amd64

kubebuilder version
Version: version.Version{KubeBuilderVersion:"2.2.0", KubernetesVendor:"1.15.5", GitCommit:"0824a139f59e109c9e418a0b6e71a53c6e9e144f", BuildDate:"2019-11-20T00:00:24Z", GoOs:"unknown", GoArch:"unknown"}

kustomize version
{Version:kustomize/v3.8.7 GitCommit:ad092cc7a91c07fdf63a2e4b7f13fa588a39af4f BuildDate:2020-11-12T01:08:43+00:00 GoOs:darwin GoArch:amd64}
```

## Steps

```
mkdir -p $GOPATH/src/github.com/nakamasato/hello-world-controller
cd ~/go/src/github.com/nakamasato/hello-world-controller
```

```
kubebuilder init --domain k8s.io
```

<details>

```
tree
.
├── Dockerfile
├── Makefile
├── PROJECT
├── README.md
├── bin
│   └── manager
├── config
│   ├── certmanager
│   │   ├── certificate.yaml
│   │   ├── kustomization.yaml
│   │   └── kustomizeconfig.yaml
│   ├── default
│   │   ├── kustomization.yaml
│   │   ├── manager_auth_proxy_patch.yaml
│   │   ├── manager_webhook_patch.yaml
│   │   └── webhookcainjection_patch.yaml
│   ├── manager
│   │   ├── kustomization.yaml
│   │   └── manager.yaml
│   ├── prometheus
│   │   ├── kustomization.yaml
│   │   └── monitor.yaml
│   ├── rbac
│   │   ├── auth_proxy_role.yaml
│   │   ├── auth_proxy_role_binding.yaml
│   │   ├── auth_proxy_service.yaml
│   │   ├── kustomization.yaml
│   │   ├── leader_election_role.yaml
│   │   ├── leader_election_role_binding.yaml
│   │   └── role_binding.yaml
│   └── webhook
│       ├── kustomization.yaml
│       ├── kustomizeconfig.yaml
│       └── service.yaml
├── go.mod
├── go.sum
├── hack
│   └── boilerplate.go.txt
└── main.go

9 directories, 30 files
```

</details>