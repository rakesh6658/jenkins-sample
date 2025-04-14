// Declarative //
pipeline {
    agent any
    options {
        timeout(time: 1, unit: 'HOURS') 
    }
    environment { 
        user = 'rakesh'
    }
    stages {
        stage('Example') {
            
            steps {
                input('Do you want to proceed?')
                echo 'Hello World'
                sh 'printenv'
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