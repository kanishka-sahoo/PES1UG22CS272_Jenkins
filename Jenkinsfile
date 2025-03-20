pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/kanishka-sahoo/PES1UG22CS272_Jenkins'
            }
        }
        stage('Build') {
            steps {
                sh 'mak -C main'
            }
        }
        stage('Test') {
            steps {
                sh './main/hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the build...'
            }
        }
    }
    
    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
