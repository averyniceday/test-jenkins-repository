pipeline {
    agent {
        docker { image 'cbioportalpipelines/cmo-pipelines:test' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'cd $CMO_PIPELINES_HOME/redcap'
                sh 'mvn clean install'
            }
        }
    }
}
