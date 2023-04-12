# Configure Cloud Deploy

## Create targets

    gcloud deploy apply \
        --region=us-central1 \
        --project=clouddeploycanary \
        --file=default-dev-target.yaml
    gcloud deploy apply \
        --region=us-central1 \
        --project=clouddeploycanary \
        --file=default-test-target.yaml
    gcloud deploy apply \
        --region=us-central1 \
        --project=clouddeploycanary \
        --file=default-prod-target.yaml

## Create delivery pipeline

    gcloud deploy apply \
        --region=us-central1 \
        --project=clouddeploycanary \
        --file=default-delivery-pipeline.yaml
