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
                sh 'mvn clean package'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests
                sh 'mvn test'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy your application
                sh 'mvn deploy'
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
