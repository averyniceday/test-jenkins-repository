pipeline {
    agent {
        docker { image 'cbioportalpipelines/cmo-pipelines:test' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'cd $CMO_PIPELINES_HOME/redcap/redcap_pipeline/target'
                sh 'java -jar redcap_pipeline.jar -e -s mskimpact_heme -d .'
            }
        }
    }
}
