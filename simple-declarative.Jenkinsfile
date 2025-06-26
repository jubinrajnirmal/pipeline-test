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
        stage('Package'){
             
            
            steps{
                echo 'Packaging the code'
            }
        }
    }
}
