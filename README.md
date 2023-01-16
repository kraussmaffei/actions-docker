# actions-docker

An action to publish docker images

## Usage

```yaml
  publish-docker-image:
    uses: kraussmaffei/actions-docker/.github/workflows/publish.yml@main
    with:
      aws-account-id: ${{ env.AWS_DEVOPS_ACCOUNT }}
      aws-region: ${{ env.AWS_DEVOPS_REGION }}
      docker-file: "Dockerfile.production"
      docker-image-version-tag: ${{ needs.publish-python-package.outputs.published-python-package-version }}
    secrets:
      pip-index-url: ${{ secrets.PIP_INDEX_URL }}
      pip-extra-index-url: ${{ secrets.PIP_EXTRA_INDEX_URL }}
```
