pipeline {
    agent any

    stages {
        stage('Ok') {
            steps {
                echo "Ok"
            }
        }
        stage('Email') {
            steps {
                emailext body: 'There has been some changed committed to the repository recently.', subject: 'New changement on the repo', to: 'houssambourkane@gmail.com'

            }
        }
    }
//     post {
//         always {
//         }
//     }
}
