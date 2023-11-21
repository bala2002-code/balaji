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
                echo 'balaji'
            }
        }
        stage('balaji') {
            steps {
                echo '20mic0113'
            }
        }
         stage('test') {
            steps {
                echo 'hello world'            }
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
