pipeline {
    agent any
	
	tools {
 		maven 'MAVEN_3'
	}
	
    stages {
        stage('Initialize') {
            steps {
                echo "Initializing pipeline..."
            }
        }

        stage('Checkout Code') {
            steps {
                echo "Cloning repository..."
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo "Executing tests..."
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
