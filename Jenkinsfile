pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                 sh 'apt-get update'
                sh 'apt-get install sshpass'
                sh 'sshpass -p "houhou10" ssh -v -tt -o "StrictHostKeyChecking no" root@10.12.177.248'
                sh 'env'
                

            }
        }
    }
}
