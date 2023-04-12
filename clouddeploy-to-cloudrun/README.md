# Create the first release

    gcloud deploy releases create release-001 \
        --region=us-central1 \
        --project=clouddeploycanary \
        --delivery-pipeline=default-delivery-pipeline \
        --skaffold-file=skaffold.yaml
