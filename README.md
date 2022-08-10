gcloud builds submit --tag gcr.io/deploy-container-358504/continous-deployment  --project=deploy-container-358504

gcloud run deploy continous-deployment --image gcr.io/deploy-container-358504/continous-deployment --platform managed  --project=deploy-container-358504 --allow-unauthenticated --region us-east1

#IAM
gcloud iam service-accounts list --project=deploy-container-358504

gcloud iam service-accounts keys create ./keys.json --iam-account email@address

gcloud auth activate-service-account --key-file=keys.json

# Useful links
* Paul Craig [blog](https://dev.to/pcraig3/quickstart-continuous-deployment-to-google-cloud-run-using-github-actions-fna)
* GitHub action [deploy-cloudrun](https://github.com/google-github-actions/deploy-cloudrun)
* Cloud Run simple Flask application [tutorial](https://cloud.google.com/run/docs/quickstarts/build-and-deploy/python)
* [Installing Google Cloud SDK](https://cloud.google.com/sdk/docs/install)