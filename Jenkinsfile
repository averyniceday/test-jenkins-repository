pipeline {
    agent {
        docker { image 'averyniceday/test-redcap:test' 
                 args '-u root' 
               }
    }
    stages {
        stage('Build') {
            steps {
                sh 'cd /app/genome-nexus-annotation-pipeline && mvn clean install'
                sh 'cd /app/cmo-pipelines && mvn clean install'
                sh 'java -jar /app/cmo-pipelines/redcap/redcap_pipeline/target/redcap_pipeline.jar -e -s mskimpact_heme -d /app/cbioportal-data/dmp/hemepact'
                sh 'java -jar /app/cmo-pipelines/redcap/redcap_pipeline/target/redcap_pipeline.jar -e -s mskimpact -d /app/cbioportal-data/dmp/mskimpact'
                sh 'ls /app/cbioportal-data/dmp/hemepact'
                sh 'sh test-file.sh /app/cbioportal-data/dmp/hemepact/data_clinical_sample.txt'
            }
        }
    }
}
