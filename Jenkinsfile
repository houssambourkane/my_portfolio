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
                    sh 'ssh -o StrictHostKeyChecking=no root@10.12.177.248 make reload_website -C /home/hbourkan/inception/'
                }
            }
        }
    }
}
