    pipeline {
        agent any
        stages {
            stage('static-analysis') {
                steps {
                    echo 'Performing static analysis'
                    script {
                        def number = input (
                            message: "Have you completed the static analysis and that has resulted in no high or critical issues??", 
                            parameters: [
                                string(name: 'Value', description: 'Enter a value equally divisble by three.')
                            ]
                        )
                    def num = number.toInteger()

                    if (num % 3 == 0) {
                        echo "Divisible by 3"
                    }else{
                        error "Not divisible by 3"
                    }    
                    }
                }
            }
            stage('build') {
                steps {
                    echo 'Building the code'
                    sleep time: 3, unit: 'SECONDS'
                }
            }
            stage('unit-test') {
                steps {
                    echo 'Running tests'
                    sleep time: 3, unit: 'SECONDS'
                }
            }
            stage('package') {
                steps {
                    echo 'Packing the application'
                    sleep time: 3, unit: 'SECONDS'
                }
            }
        
        }
    }
