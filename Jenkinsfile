pipeline {
    agent {
        docker { image 'averyniceday/redcap:test' 
                 args '-u root' 
               }
    }
    stages {
        stage('Build') {
            steps {
                sh 'cd /app/genome-nexus-annotation-pipeline && mvn clean install'
                sh 'cd /app/cmo-pipelines && mvn clean install'
                sh 'java -jar /app/cmo-pipelines/redcap/redcap_pipeline/target/redcap_pipeline.jar -e -s mskimpact_heme -d .'
            }
        }
    }
}
