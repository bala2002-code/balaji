pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Assuming your Git integration is already set up
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Define Maven tool installation
                def mvnHome = tool 'Maven3'

                // Run Maven build
                sh "${mvnHome}/bin/mvn clean install"
            }
        }

        stage('Test') {
            steps {
                echo 'Run tests'
                // Add commands to run your tests if applicable
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy app'
                // Add commands for deployment if applicable
            }
        }
    }

    post {
        always {
            emailext body: 'summary', subject: 'Pipeline Status', to: 'balaji.g2020@vitstudent.ac.in'
        }
    }
}
