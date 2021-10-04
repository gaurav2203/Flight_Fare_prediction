pipeline{
    agent any
    stages{
        stage("infrastructure"){
            steps{
                sh -c 'cd ./gcloud && terraform apply -var-file="variable.fvars" --auto-approve'
                sh -c 'gcloud container clusters get-credentials prediction_app --region=us-central1 --project=encoded-rider-325715'
            }
        }
        stage("Launching deployment"){
            steps{
                echo "till here working fine!!!!!!!!!!!!"
            }
        }
    }
}
