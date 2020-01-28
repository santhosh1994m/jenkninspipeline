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
                sh 'if [ -d DEMO_ECS_S3_Dynamo_Terraform_Code ]; then  rm -rf DEMO_ECS_S3_Dynamo_Terraform_Code; fi'
            }
        }
        
        stage('git clone') {
            steps {
                sh 'git clone https://github.com/amitvermaa93/jenkins-git-integration.git'
            }
        }
        
         stage('sleep') {
            steps {
                sh 'sleep 10'
            }
        }
        
    }
}
