# scan-image-action

This action combines the trivy sec scanning for IaC and image and pushes it to a remote repo.

Usage in a github `workflow.yml` file:

```yaml
- uses: DeluxeOwl/scan-image-action@v1
  with:
    image-name: test_image
    image-version: v0.1
    registry: ghcr.io
    registry-username: username
    registry-password: password
    severity: "CRITICAL"
```

Optional parameters:

```yaml
# CRITICAL,HIGH etc. separated by comma (no space)
# defaults to CRITICAL
severity: "CRITICAL, HIGH"
```
