pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'build app'
            
            }
        }
        stage('this') {
            steps {
                echo 'sriram'
            }
        }
        stage('balaji') {
            steps {
                echo '20mic0159'
            }
        }
         stage('test') {
            steps {
                echo 'test app'
            }
        }
         stage('deploy') {
            steps {
                echo 'deploy app'
            }
        }
        
    }
        
    post
    {
        always
        {
            emailext body: 'summary', subject: 'pipeline status', to: 'balaji.g2020@vitstudent.ac.in'
        }
    }
}
