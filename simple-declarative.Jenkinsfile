pipeline{
    agent any

    parameters {
        string(name: 'branch', defaultValue: 'main', description: 'Branch to fetch for pipeline')
    }

  
    stages {
        stage('SCM'){
            steps{
                git branch: "${params.branch}", url: 'https://github.com/jubinrajnirmal/pipeline-test.git'
            }    
        }
        stage('Static analysis'){
            steps{
                echo 'Performing static analysis'
                sleep time:3, unit:'SECONDS'
            }
        }
        stage('build'){
            steps{
                echo 'Building the code'
                sleep time:3, unit:'SECONDS'
            }
        }
        stage('unit test'){
            steps{
                echo 'executing unit tests'
                sleep time:3, unit:'SECONDS'
            }
        }
        stage('Package'){
            steps{
                echo 'Packaging the code'
                sleep time:3, unit:'SECONDS'
            }
        }
    }
}
