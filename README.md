gcloud builds submit --tag gcr.io/resolute-radar-357007/continous-deployment  --project=resolute-radar-357007

gcloud run deploy continous-deployment --image gcr.io/resolute-radar-357007/continous-deployment --platform managed  --project=resolute-radar-357007 --allow-unauthenticated --region us-east1

#IAM
gcloud iam service-accounts list --project=resolute-radar-357007

gcloud iam service-accounts keys create ./keys.json --iam-account github-actions@resolute-radar-357007.iam.gserviceaccount.com

gcloud auth activate-service-account --key-file=keys.json

# Useful links
* Paul Craig [blog](https://dev.to/pcraig3/quickstart-continuous-deployment-to-google-cloud-run-using-github-actions-fna)
* GitHub action [deploy-cloudrun](https://github.com/google-github-actions/deploy-cloudrun)
* Cloud Run simple Flask application [tutorial](https://cloud.google.com/run/docs/quickstarts/build-and-deploy/python)
* [Installing Google Cloud SDK](https://cloud.google.com/sdk/docs/install)