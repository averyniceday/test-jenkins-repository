pipeline {
    agent {
        docker { image 'averyniceday/redcap:test' 
                 args '-u root' 
               }
    }
    stages {
        stage('Test') {
            steps {
                sh 'java -jar /app/cmo-pipelines/redcap/redcap_pipeline/target/redcap_pipeline.jar -e -s mskimpact_heme -d .'
            }
        }
    }
}
