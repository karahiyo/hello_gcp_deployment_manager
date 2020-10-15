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

### Create vm

```sh
$ gcloud deployment-manager deployments create quickstart-deployment --config examples/v2/quick_start/vm.yaml
```

### Create vm with template

```sh
$ gcloud deployment-manager deployments create a-single-vm-with-template --template examples/v2/build_configuration/add_templates/jinja/vm-template.jinja --properties zone:us-central1-a
```

### Delete deployment

```sh
$ gcloud deployment-manager deployments delete <deployment-name>
```

### Access control

```sh
$ gcloud deployment-manager deployments create pubsub-access-control --template examples/v2/access_control/access_control.jinja --preview
```

### Mongo
```sh
$ gcloud deployment-manager deployments create hello-deployment-manager-mongo --template examples/v2/mongo/mongo.jinja --preview
```

### Cloud Function

https://github.com/GoogleCloudPlatform/deploymentmanager-samples/tree/master/google/resource-snippets/cloudfunctions-v1

```sh
$ gcloud deployment-manager deployments create hello-deployment-manager-cloud-functions --template examples/v2/cloud_function/cloud_functions.jinja --preview --properties region:ap-northeast,entryPoint:dummy-entrypoint,runtime:python3.8
```



## gcloud deployment-manager command

### list tyes

```
$ gcloud deployment-manager types list
```

### preview

```sh
$ gcloud deployment-manager deployments create a-single-vm-with-template --template examples/v2/build_configuration/add_templates/jinja/vm-template.jinja --properties zone:us-central1-a --preview
...

NAME                          TYPE            STATE       ERRORS  INTENT
vm-a-single-vm-with-template  compute.v1.instance  IN_PREVIEW  []      CREATE_OR_ACQUIRE
```

