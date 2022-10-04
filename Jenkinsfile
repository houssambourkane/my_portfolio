pipeline {
    agent any

    stages {
        stage('Email') {
            steps {
                emailext body: 'Your repository has been modified recently !.', subject: 'Repository trigger notification', to: 'houssambourkane@zohomail.com'
            }
        }
        stage('Pushing') {
            steps {
                sshagent(credentials : ['remote-server-ssh-key']) {
                    sh 'ssh -o StrictHostKeyChecking=no root@10.12.177.248 usermod -aG docker jenkins'
                    sh 'ssh -o StrictHostKeyChecking=no root@10.12.177.248 aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 494732116747.dkr.ecr.us-east-1.amazonaws.com'
                    sh 'ssh -o StrictHostKeyChecking=no root@10.12.177.248 docker tag srcs_wordpress:latest 494732116747.dkr.ecr.us-east-1.amazonaws.com/wordpress:latest'
                    sh 'ssh -o StrictHostKeyChecking=no root@10.12.177.248 docker push 494732116747.dkr.ecr.us-east-1.amazonaws.com/wordpress:latest'
                }
            }
        }
    }
}
