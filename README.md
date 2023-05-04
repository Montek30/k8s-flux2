# flux-example

# Flux Upgrade from v0.41.2 to v2.0.0-rc.1


Key Features of v0.41.2:

 Promotion of GitOps related APIs to v1:

GitRepository

Kustomization

Receiver

Horizontal scaling & sharding to Flux controllers

 

Steps :

 Upgrading GitRepository to v1

 set apiVersion: source.toolkit.fluxcd.io/v1 in the YAML files that contain GitRepository definitions and remove the deprecated fields:

    the deprecated field .spec.gitImplementation was removed

    the unused field .spec.accessFrom was removed

    the deprecated field .status.contentConfigChecksum was removed

    the deprecated field .status.artifact.checksum was removed

    the .status.url was removed in favor of the absolute .status.artifact.url

Upgrading Kustomization to v1

set apiVersion: kustomize.toolkit.fluxcd.io/v1 in the YAML files that contain Kustomization definitions and remove the deprecated fields if any

the deprecated field .spec.validation was removed

the deprecated field .spec.patchesStrategicMerge was removed (replaced by .spec.patches)

the deprecated field .spec.patchesJson6902 was removed (replaced by .spec.patches).

Upgrading Receiver to v1

set apiVersion: notification.toolkit.fluxcd.io/v1 in the YAML files that contain Receiver definitions

no fields were removed.
