// Declarative //
pipeline {
    agent { label 'agent' }
    options {
         ansiColor('xterm')
    }
    stages {
        stage('Example') {
            input {
                message "should we continue?"
            }
            steps {
                echo 'Hello World'
                
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success {
            echo"script is success"
        }
        failure{
            echo "script is failure"
        }
    }
}