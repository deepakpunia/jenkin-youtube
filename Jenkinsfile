pipeline {
    agent any
    environment {
        name = 'Deepak'
    }

    stages {
        stage('Run A command') {
            environment {
               name = 'Deepak'
            }
            steps {
                sh '''
                ls
                date
                pwd
                echo ${name}
                calendar
                '''
            }
        }
        stage('Enviroment Variable') {
            environment {
               name = 'Himank'
            }
            steps {
                sh 'echo "${BUILD_ID}"'
                sh 'echo ${name}'
            }
        }
        stage('Containue') {
            input {
                message "Should we Containue?"
                ok "Yes we should"
            }
            steps {
                echo 'Deploy on test'
            }
        }
        stage('Deploy on Prod') {
            steps {
                echo 'Deploy on Prod'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'Failure'
        }
        success { 
            echo 'Success'
        }
    }
}
