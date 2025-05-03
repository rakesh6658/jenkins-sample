// Declarative //
pipeline {
    agent any
    options{
        timeout(time: 2, unit: 'HOURS')
    }
    
environment { 
        user ='rakesh'
    }
    

    stages {
        stage('Example') {
            environment {
                AN_ACCESS_KEY = credentials('ssh-auth') 
            }
            steps {
                sh 'printenv'
                
                
            }
        }

        stage('Example Deploy') {
           
            steps {
                echo 'Deploying'
            }
        }
    }
    

    post {
        always{
            echo 'pipeline is   success dubbu'
        }
        success{
           echo 'pipeline is success rakesh'
        }
        
    
    }
}
