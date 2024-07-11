# practice

$ gcloud iam roles create artifactRegistryCIRole --project=$PROJECT_ID --title="Docker image CI Role" --description="Push docker image via CI" --permissions=artifactregistry.repositories.uploadArtifacts --stage=BETA

$ gcloud projects add-iam-policy-binding $PROJECT_ID --member=serviceAccount:docker-image-ci@$PROJECT_ID.iam.gserviceaccount.com --role=projects/$PROJECT_ID/roles/artifactRegistryCIRole
