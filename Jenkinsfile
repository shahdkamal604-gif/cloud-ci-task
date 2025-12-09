pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // ينزل الكود من GitHub
                checkout scm
            }
        }

        stage('Build & Test') {
            steps {
                // على الماك / لينكس نستخدم sh
                sh 'mvn -B test'
            }
        }
    }

    post {
        success {
            echo 'Build & tests passed successfully!'
        }
        failure {
            echo 'Build or tests failed!'
        }
    }
}

