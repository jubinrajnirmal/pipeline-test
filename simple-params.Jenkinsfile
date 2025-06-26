pipeline{
    agent any
    
    parameters { 
        text(name:'multiline', defaultValue: 'This is a multiline value for the parameter')
        booleanParam(name: 'isAdmin', defaultValue: false, description: 'Is the user an admin?')
        choice(name: 'targetEnvironment', choices: ['dev', 'staging', 'qa', 'production'], description: 'Select the target environment')
    }

    stages{
        stage('pre-flight'){
            steps{
                echo "Text: ${params.multiline}"
                echo "Is current user an admin? ${params.isAdmin ? 'Yes' : 'No' }"
                echo "Target Environment: ${params.targetEnvironment}"
            }
        }
    }


}