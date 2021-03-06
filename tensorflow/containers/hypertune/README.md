
## Introduction

This sample shows how to run hyperparameter tuning jobs on AI Platform with tf estimators inside custom containers [cloudml-hypertune package](https://pypi.org/project/cloudml-hypertune/).

This sample is adapted from [the official samples for tuning ResNet-50 with Cloud TPUs on AI Platform](https://github.com/ultrons/cloudml-samples/tree/master/tpu/hptuning/resnet-hypertune)


## Requirements

- Install [Google Cloud Platform SDK](https://cloud.google.com/sdk/).  The SDK includes the commandline tools `gcloud` for submitting training jobs to [AI Platform](https://cloud.google.com/ml-engine/).

- Enable [Cloud Storage](https://cloud.google.com/storage).

## Steps

1. Clone the repository.

    ```
    git clone https://github.com/GoogleCloudPlatform/cloudml-samples.git
    ```

1. If you do not already have a Cloud Storage bucket, create one to be used for the training job.

    ```
    gsutil mb gs://[YOUR_GCS_BUCKET]
    export GCS_BUCKET="gs://[YOUR_GCS_BUCKET]"
    ```

1. Run the sample.  The included script will train ResNet-50 for 1024 steps using a fake dataset.

    ```
    cd cloudml-samples/tensorflow/containers/hypertune
    bash submit_resnet_hypertune.sh
    ```
