# hello_gcp_deployment_manager

https://cloud.google.com/deployment-manager/docs/quickstart

## Examples

### gcloud deployment-manager deployments create --help

```
$ gcloud deployment-manager deployments create --help

NAME
    gcloud deployment-manager deployments create - create a deployment

SYNOPSIS
    gcloud deployment-manager deployments create DEPLOYMENT_NAME
        (--composite-type=COMPOSITE_TYPE | --config=CONFIG
          | --template=TEMPLATE) [--description=DESCRIPTION]
        [--labels=[KEY=VALUE,...]] [--preview] [--properties=[PROPERTIES,...]]
        [--async | --automatic-rollback-on-error] [GCLOUD_WIDE_FLAG ...]

DESCRIPTION
    This command inserts (creates) a new deployment based on a provided config
    file.

...
```

### create vm

```
gcloud deployment-manager deployments create quickstart-deployment --config examples/v2/quick_start/vm.yaml
```
