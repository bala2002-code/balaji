pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Define Maven tool installation
                    def mvnHome = tool 'Maven3'

                    // Run Maven build
                    sh "${mvnHome}/bin/mvn clean install"
                }
            }
        }

        // Add other stages as needed

        stage('Hello World') {
            steps {
                echo 'Hello, World!'
            }
        }
    }

    post {
        always {
            emailext body: 'summary', subject: 'Pipeline Status', to: 'balaji.g2020@vitstudent.ac.in'
        }
    }
}
