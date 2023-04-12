# Build Application

## Auth

    gcloud auth login
    gcloud auth configure-docker us-docker.pkg.dev

## Build

    docker build --platform linux/amd64 --no-cache -t us-docker.pkg.dev/clouddeploycanary/default/app .

## Push

    docker push us-docker.pkg.dev/clouddeploycanary/default/app
