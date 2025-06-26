pipeline{
    agent any

    parameters {
        string(name: 'branch', defaultValue: 'main', description: 'Branch to fetch for pipeline')
    }
    triggers {
        cron('0 3 * * 1-5')
    }
  
    stages {
        stage('SCM'){
            steps{
                git branch: 'main', url: 'https://github.com/jubinrajnirmal/pipeline-test.git'
            }    
        }
        stage('Package'){
            when{
                expression {
                    return params.brach == 'release'
                }
            }
            steps{
                echo 'Packaging the code'
            }
        }
    }
}
