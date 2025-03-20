pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git url: 'https://github.com/kanishka-sahoo/PES1UG22CS272_Jenkins'
            }
        }
        stage('Build') {
            steps {
                // Build using make command in the main directory
                sh 'make -C main'
            }
        }
        stage('Test') {
            steps {
                // Run the generated executable and print its output
                sh './main/PES1UG22CS272-1'
            }
        }
        stage('Deploy') {
            steps {
                // Placeholder for deploy steps
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
