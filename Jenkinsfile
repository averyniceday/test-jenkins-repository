pipeline {
    agent {
        docker { image 'cbioportalpipelines/cmo-pipelines:test' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'java -jar redcap_pipeline.jar -e -s mskimpact_heme -d .'
            }
        }
    }
}
