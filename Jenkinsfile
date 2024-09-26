pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Clone your Git repository
                git url: 'https://github.com/votre-utilisateur/votre-repo.git', branch: 'main'
            }
        }

        stage('Build with Maven') {
            steps {
                // Compile and build the project using Maven
                sh 'mvn clean install'
            }
        }

        stage('Test Application') {
            steps {
                // Run unit tests
                sh 'mvn test'
            }
        }

        stage('Hello World') {
            steps {
                // Print "Hello World"
                echo 'Hello World'
            }
        }
    }

    post {
        always {
            // Cleanup or actions to run after the pipeline (e.g., archiving logs)
            echo 'Pipeline completed.'
        }
    }
}
