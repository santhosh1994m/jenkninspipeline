pipeline {
    agent {
        node {
            label 'master'
        }
    }


    stages {


        stage('terraform started') {
            steps {
                sh 'echo "Started...!" '
            }
        }
        
        stage('chage path') {
            steps {
                sh 'if [ -d terraformpipeline ]; then  rm -rf terraformpipeline; fi'
            }
        }
        
        stage('git clone') {
            steps {
                sh 'git clone https://github.com/santhosh1994m/DEMO_ECS_S3_Dynamo_Terraform_Code.git'
            }
        }
        
         stage('sleep') {
            steps {
                sh 'sleep 10'
            }
        }
        
        stage('terraform init') {
            steps {
                sh 'sudo /usr/local/bin/terraform init ./terraformpipeline'
            }
        }
        stage('terraform plan') {
            steps {
                sh 'sudo /usr/local/bin/terraform plan ./terraformpipeline'
            }
        }
        stage('terraform ended') {
            steps {
                sh 'echo "Ended....!!"'
            }
        }


        
    }
}
