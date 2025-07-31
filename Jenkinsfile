pipeline {
    agent any
    environment { 
        name = 'rakesh'
    }
    options{
        timeout(time: 1, unit: 'HOURS')
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh'printenv'
            }
             environment { 
                auth = credentials('ssh-auth') 
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh'printenv'
            }
        }
    }
     post {
        always {
            echo 'This will always run (success or failure)'
        }
        success {
            echo 'This will run only if the pipeline succeeded from webhook'
        }
        failure {
            echo 'This will run only if the pipeline failed'
        }
        unstable {
            echo 'This will run if the build is unstable'
        }
        changed {
            echo 'This will run if the build status changed from the last run'
        }
        cleanup {
            echo 'This will run at the end for any necessary cleanup'
        }
    }
}


