# eng24cs0233-jenkins-lab
stage('Docker image') {
    steps {
        sh 'docker build -t ${APP_NAME}:${BUILD_NUMBER} .'
        sh 'docker run --rm ${APP_NAME}:${BUILD_NUMBER}'
        sh 'docker images ${APP_NAME}'
    }
}
