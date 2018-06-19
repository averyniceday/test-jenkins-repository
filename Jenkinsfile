pipeline {
    agent {
        docker { image 'cbioportalpipelines/cmo-pipelines:test' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'cd $CMO_PIPELINES/redcap'
                sh 'mvn clean install'
            }
        }
    }
}
