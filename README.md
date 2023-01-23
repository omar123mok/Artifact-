
# Artifact-

Creates and uploads an Artifact of the current repository.

## Event

Triggered by push

## Code

The Workflow script.


```yaml
name: artifact

on: push

env:
  ARTIFACT_NAME: my-artifact

jobs:
  job1:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout the repo
        uses: actions/checkout@v2
      - name: Upload the artifact
        uses: actions/upload-artifact@v2
        with:
          name: ${{ env.ARTIFACT_NAME }}
          path: .
```

Jobs: job1 has 2 steps:

1 . Checkout the repository

2 . Upload the artifact, the artifact name is provided via the env variable ARTIFACT_NAME.


Example.
```
env:
  ARTIFACT_NAME: my-artifact

```
