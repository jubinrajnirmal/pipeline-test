pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Build the code'
            }
        }
        stage('Notify'){
            steps{
                echo "Send notification to Slack"
                slackSend channel: 'devops', message: 'build completed'
            }
        }
    }
}