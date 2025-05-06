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
        stage('condition'){
            
                when {
                 environment name: 'user', value: 'dubbu'
            }
            steps {
                echo 'This runs only on main branch'
            }

            }
        

        stage('Example Deploy') {
           
            steps {
                echo 'Deploying'
            }
            
             input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
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
