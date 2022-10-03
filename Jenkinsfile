pipeline {
    agent any

    stages {
        stage('Email') {
            steps {
                emailext body: 'There has been some changed committed to the repository recently.', subject: 'New changement on the repo', to: 'houssambourkane@zohomail.com'

            }
        }
    }
//     post {
//         always {
//         }
//     }
}
