
pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build and Test') {
            steps {
                bat 'mvn -B clean verify'
            }
        }
    }

    post {
        success {
            echo 'ProductInvoice pipeline completed successfully!'
        }

        failure {
            echo 'ProductInvoice pipeline failed. Check the console output.'
        }
    }
}
