pipeline{
    agent {label "aero"}

    triggers {
        cron('0 3 * * 1-5')
    }
  
    stages {
        stage('SCM'){
            steps{
                git branch: 'main', url: 'https://github.com/jubinrajnirmal/pipeline-test.git'
            }    
        }
    }
}
