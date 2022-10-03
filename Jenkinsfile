pipeline {
    agent any

    stages {
        stage('Email') {
            steps {
                emailext body: 'Check of the repository is made every minute.', subject: 'Check', to: 'houssambourkane@zohomail.com'

            }
        }
    }
}
