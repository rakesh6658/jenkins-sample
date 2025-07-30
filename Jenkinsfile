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
                echo 'Deploying...'
            }
        }
    }
}
