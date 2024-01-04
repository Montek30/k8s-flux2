# Flux
Flux - the GitOps family of projects
Flux version v2.2.2
Flux is a set of continuous and progressive delivery solutions for Kubernetes that are open and extensible. Flux is a CNCF Graduated project.

Flux docs: https://fluxcd.io/flux/

Install cli

```
# install cli
brew install fluxcd/tap/flux
# or
curl -s https://fluxcd.io/install.sh | sudo bash
# check version
flux --version
```

# bootstrap flux
flux bootstrap github --owner=Montek30 --repository=k8s-flux2-and-components --path=./ --branch=main --components-extra=image-reflector-controller,image-automation-controller
