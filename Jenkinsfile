pipeline{
    agent any
    tools {
        terraform 'terraform'
    }
    stages{
        stage('checkout from GIT'){
            steps{
               git branch: 'main', url: 'https://github.com/sanju-0712/jenkins-terraformcicd.git'
            }
        }
        stage('Terraform Init'){
            steps{
                sh 'terraform init'
            }
        }
        stage('Terraform Plan'){
            steps{
                sh 'terraform plan'
            }
        }
         stage('Terraform Apply'){
            steps{
                sh 'terraform apply --auto-approve'
            }
        }
         stage('Terraform Destroy'){
            steps{
                sh 'terraform destroy --auto-approve'
            }
         }
       
    }
}
