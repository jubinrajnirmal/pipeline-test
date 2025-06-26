pipeline {
    agent any

 

    stages {
        
        stage('parallel phases') {
            parallel {
                stage('static analysis') {
                    steps {
                        echo 'Performing static analysis'
                        sleep time: 3, unit: 'SECONDS'
                    }
                }
                stage('build and test') {
                    stages {
                        stage('build') {
                            steps {
                                echo 'Building the code'
                                sleep time: 3, unit: 'SECONDS'
                            }
                        }
                        stage('unit test') {
                            steps {
                                echo 'executing unit tests'
                                sleep time: 3, unit: 'SECONDS'
                            }
                        }
                    }
                }
            }
        }
        stage('Package') {
            when {
                expression {
                    return params.branch == 'release'
                }
            }
            steps {
                echo 'Packaging the code'
                sleep time: 3, unit: 'SECONDS'
            }
        }
    }
}
