pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh '''
                    ls -lahtr
                    touch yes.txt
                '''
            }
        }
        stage('With docker'){
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                   ls -lahtr
                '''
                }
        }
    }
}
