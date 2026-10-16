node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker rm -f samplerunning || true'
        }
    }
    stage('Build') {
        build 'BuildSampleApp'
    }
    stage('Results') {
        build 'TestSampleApp'
    }
}
