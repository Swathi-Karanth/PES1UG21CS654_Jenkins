pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ PES1UG21CS654-1.cpp -o PES1UG21CS654-1'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    python server.py    // error!
                    sh './PES1UG21CS654-1'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
