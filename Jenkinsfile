pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sshagent(credentials : ['ssh-key-portfolio']) {
                    sh 'ssh -o StrictHostKeyChecking=no root@10.12.177.248 uptime'
                    sh 'ssh -v root@10.12.177.248'
                    sh 'env'
                }
            }
        }
    }
}
