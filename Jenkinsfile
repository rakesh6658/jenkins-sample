pipeline {
    agent any
    environment { 
        name = 'rakesh'
    }
    options{
        timeout(time: 1, unit: 'HOURS')
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


