pipeline {
 agent any
 
 stages {
 stage(‘checkout’) {
 steps {
 git branch: ‘master’, url: ‘github.com/santhosh1994m/DEMO_ECS_S3_Dynamo_Terraform_Code.git’
 
 }
 }
 //stage(‘SetTerraform’) {
 //steps {
 //cript {
 //def tfHome = tool name: ‘Terraform’
 //env.PATH = “${tfHome}:${env.PATH}”
 //}
 //sh ‘terraform — version’
 //}
 //}
 
 stage(‘Provisioninfrastructure’) {
 
 steps {
 dir(‘DEMO_ECS_S3_Dynamo_Terraform_Code’)
 {
 sh ‘terraform init’
 sh ‘terraform plan’
 // sh ‘terraform destroy -auto-approve’
 //sh ‘terraform apply plan’
 }
 
 
 }
 }
  
 }
}
