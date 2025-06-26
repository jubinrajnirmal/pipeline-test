pipeline{
    agent any


    triggers {
        cron('0 3 * * 1-5')
    }
  
    stages {
        stage('build'){
            steps{
                echo 'Building the code'
            }
        }
        }
        stage('Package'){
            when{
                expression {
                    return params.branch == 'release'
                }
            }
            steps{
                echo 'Packaging the code'
            }
        }
    }
}
