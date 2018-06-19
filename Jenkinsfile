pipeline {
    agent {
        docker { image 'cbioportalpipelines/cmo-pipelines:test' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'java -jar $CMO_PIPELINES_HOME/redcap/redcap_pipeline/target/redcap_pipeline.jar -e -s mskimpact_heme -d .'
            }
        }
    }
}
