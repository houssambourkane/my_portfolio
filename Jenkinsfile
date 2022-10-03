pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sshagent(credentials : ['remote-server-ssh-key']) {
                sh 'ssh -o StrictHostKeyChecking=no root@10.12.177.248 uptime'
                sh 'ssh -v root@10.12.177.248'
                sh 'scp /home root@10.12.177.248:/home/houss/inception/'
                }

            }
        }
    }
}
