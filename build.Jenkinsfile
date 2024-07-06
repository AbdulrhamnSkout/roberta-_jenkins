pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'echo start building...'
                sh 'echo ${env.DOCKER_PASSWORD} '
                sh 'docker login -u abd0525656@gmail.com -p ${env.DOCKER_PASSWORD}'
                sh 'docker build -t bdskcot/jenkins_test_repo:${env.BUILD_NUMBER} .'
                sh 'docker push abdskcot/jenkins_test_repo:${env.BUILD_NUMBER}'

            }
        }
    }

}
