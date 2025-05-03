// Declarative //
pipeline {
    agent any
    
environment { 
        user ='rakesh'
    }
    

    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
                
                
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
