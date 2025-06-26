pipeline {
    agent any
    stages {
        stage('static-analysis') {
            steps {
                echo 'Performing static analysis'
                script {
                    input message: "Have you completed the static analysis and that has resulted in no high or critical issues??", 
                          ok: "Yes, I have completed it"
                }
            }
        stage('build') {
            steps {
                echo 'Building the code'
                sleep time: 3, unit: 'SECONDS'
            }
        }
        stage('unit-test') {
            steps {
                echo 'Running tests'
                sleep time: 3, unit: 'SECONDS'
            }
        }
        stage('package') {
            steps {
                echo 'Packing the application'
                sleep time: 3, unit: 'SECONDS'
            }
        }
    }
    }
}
