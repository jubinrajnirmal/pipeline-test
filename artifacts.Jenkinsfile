pipeline{
    agent any
    environment {
        ARTIFACT_SOURCE_DIRECTORY = 'tests/*.xml'
    }
    stages  {
        stage('Build'){
            steps{
                echo 'Build the code'
            }
        }
        stage('test'){
            steps{
                echo "Executing Tests"
                sh "mkdir -p tests && echo 'Test results' > tests/test-results.xml"
                error "broken test break the build"
        }   }
    }
    post{
        always {
            archiveArtifacts artifacts: ARTIFACT_SOURCE_DIRECTORY, followSymlinks: false
        }
    }
}
