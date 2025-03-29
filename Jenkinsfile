// Declarative //
pipeline {
    agent { label 'agent' }
    options {
         ansiColor('xterm')
    }
    stages {
        stage('Example') {
            
            steps {
                input('Do you want to proceed?')
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