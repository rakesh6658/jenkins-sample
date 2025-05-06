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
         stage('Parallel Stage') {
            parallel {
                stage('Branch A') {
                    
                    steps {
                        echo "On Branch A"
                    }
                }
                stage('Branch B') {
                   
                    steps {
                        echo "On Branch B"
                    }
                }
                stage('Branch C') {
                    
                    stages {
                        stage('Nested 1') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                            }
                        }
                        stage('Nested 2') {
                            steps {
                                echo "In stage Nested 2 within Branch C"
                            }
                        }
                    }
                }
            }
        }
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
    
    

    post {
        always{
            echo 'pipeline is   success dubbu'
        }
        success{
           echo 'pipeline is success rakesh'
        }
        
    
    }
}
