// Declarative //
pipeline {
    agent any
    options{
        timeout(time: 2, unit: 'HOURS')
    }
    
    
environment { 
        user ='rakesh'
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    

    stages {
        stage('Example') {
            environment {
                AN_ACCESS_KEY = credentials('ssh-auth') 
            }
            steps {
                sh 'printenv'
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
                
                
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
