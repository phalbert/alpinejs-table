pipeline {
    agent any

    environment {
        GITHUB_TOKEN = credentials("GITHUB_LIMBOPAY")
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'git@github.com:limbopay/limbo-core.git'
            }
        }
        
        stage('Publish results') {
            steps {
                echo "Deployment successful"
            }
        }
    }

    post {
        success {
            echo "Build successful"
            // You can add additional steps here, like running tests or notifications.
        }

        failure {
            echo "Build failed"
        }
    }
}
