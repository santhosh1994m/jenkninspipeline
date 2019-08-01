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
                sh 'if [ -d jenkinspocpipeline ]; then sudo rm -rf jenkinspocpipeline; fi'
            }
        }
        
        stage('git clone') {
            steps {
                sh 'sudo git clone https://github.com/shibir07/jenkinspocpipeline.git'
            }
        }
        
         stage('sleep') {
            steps {
                sh 'sleep 10'
            }
        }
        
        stage('terraform init') {
            steps {
                sh 'sudo /usr/local/bin/terraform init ./jenkinspocpipeline'
            }
        }
        stage('terraform plan') {
            steps {
                sh 'sudo /usr/local/bin/terraform plan ./jenkinspocpipeline'
            }
        }
        stage('terraform ended') {
            steps {
                sh 'echo "Ended....!!"'
            }
        }


        
    }
}
