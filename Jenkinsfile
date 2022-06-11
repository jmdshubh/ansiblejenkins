pipeline {
    agent {
        label 'agentnode1'
    }
    stages {
        stage('checkout'){
            steps {
                git credentialsId: 'githubtechsriman', url: 'https://github.com/techsriman/ansiblejenkins.git'
            }
        }
        stage('playbook') {
            steps {
                
                ansiblePlaybook(credentialsId: 'agentsshkey', inventory: 'hosts', playbook: 'user-playbook.yaml')
                
               
               
            }
        }
    }
}