pipeline {
    agent any

    stages{
        stage('deploy to S3'){
            steps{
               sh 'aws s3 cp public s3://bucket817148 --recursive'
               sh 'aws s3api put-bucket-policy --bucket bucket817148 --policy file://policy.json'
               sh 'aws s3 website s3://bucket817148/ --index-document index.html '
             
            }
        }
    }
    
}
