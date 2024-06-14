pipeline {
    agent any
    stages {
        stage('clean old containers & images up ') {
            steps {
                echo "clean old containers"
                sh "docker rm -f \$(docker ps -qa) || true"
                echo "clean old images"
                sh "docker rmi -f \$(docker images) || true"
            }
        }
         stage('Build step') {
            steps {
                sh "sh setup.sh"
            }
        }
    }
}
