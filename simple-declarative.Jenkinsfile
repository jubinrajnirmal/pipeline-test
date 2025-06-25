pipeline{
    agent any
    
    environment {
        SENTENCE = "Holy Moly Sheep"
    }
    stages {
        stage('Hello'){
            steps{
                echo 'Hello World!'
                script {
                    def words = env.SENTENCE.split(' ')
                    for (word in words){
                        echo word
                    }
                }
            }
        }
    }
}