pipeline {
    agent { label 'agent-1' }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'ee
            }
        }
    }
     post {
        always {
            echo 'This will always run (success or failure)'
        }
        success {
            echo 'This will run only if the pipeline succeeded'
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


