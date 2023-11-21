pipeline {
    agent any

    stages {
     
        stage('Build with Maven in Docker') {
            steps {
                script {
                    // Define Maven tool installation
                    def mvnHome = tool 'Maven3'

                    // Run Maven build inside a Maven Docker container
                    docker.image('maven:3-alpine').inside('-v $HOME/.m2:/root/.m2') {
                        // Copy the Maven settings.xml file if needed
                        sh 'cp /usr/share/maven/ref/settings-docker.xml $HOME/.m2/settings.xml'
                        
                        // Run Maven build
                        sh "${mvnHome}/bin/mvn clean install"
                    }
                }
            }
        }

       
    }

    post {
        always {
            emailext body: 'summary', subject: 'Pipeline Status', to: 'balaji.g2020@vitstudent.ac.in'
        }
    }
}
