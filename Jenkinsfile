pipeline {
    agent any
    stages{
        stage('SCM checkout'){
            steps{
                 git 'https://github.com/thangSu/demo-ansible-jenkins.git'
            }
        }
        stage('excute ansible '){
            steps{
                ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'ansible', inventory: 'hosts', playbook: 'apache.yaml'
            }
        }
               

        
    }
}