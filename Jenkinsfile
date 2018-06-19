pipeline {
    agent {
        docker { image 'cbioportalpipelines/cmo-pipelines:test }
    }
    stages {
        stage('Test') {
            steps {
                java -jar redcap_pipeline.jar -e -s mskimpact -d .
            }
        }
    }
}
