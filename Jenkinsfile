pipeline {
    agent any

    stages {
        stage('Email') {
            steps {
                emailext body: 'Your repository has been modified recently !.', subject: 'Repository trigger notification', to: 'houssambourkane@zohomail.com'
            }
        }
    }
}
