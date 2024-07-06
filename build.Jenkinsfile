pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'echo start building...'
                sh 'echo "$DOCKER_PASSWORD" | docker login -u abd0525656@gmail.com --password-stdin'
                sh 'docker build -t ${env.BUILD_NUMBER} .'
                sh 'docker push abdskcot/jenkins_test_repo:${env.BUILD_NUMBER}'
            }
        }
    }
}