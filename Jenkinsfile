pipeline {
    agent {
        docker { image 'cbioportalpipelines/cmo-pipelines:test' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'cd $CMO_PIPELINES_HOME/redcap/redcap_pipeline/'
                sh 'ls'
                sh 'cd target'
                sh 'java -jar redcap_pipeline.jar -e -s mskimpact_heme -d .'
            }
        }
    }
}
