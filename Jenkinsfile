pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project...'
                    sh 'make -C nonexistent_directory'  
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sh 'cd /var/jenkins_home/workspace/PES2UG22CS356-1/main/ && ./hello_exec'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed due to an error in one of the stages!'
        }
    }
}
