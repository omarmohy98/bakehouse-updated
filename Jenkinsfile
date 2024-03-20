pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                // Build your project here
                echo 'Building'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests
                echo 'Testing'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy your application
                echo 'Deploying'
            }
        }
    }
    
    // Post-build actions
    post {
        success {
            echo 'Build successful! You can do further actions here.'
        }
        failure {
            echo 'Build failed! You may need to take corrective actions.'
        }
        always {
            echo 'This stage will always be executed.'
        }
    }
}
