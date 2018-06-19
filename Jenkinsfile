pipeline {
    agent {
        docker { image 'averyniceday/redcap:Test' 
                 args '-u root' 
               }
    }
    stages {
        stage('Test') {
            steps {
                sh 'cd /app/cmo-pipelines/redcap && mvn clean install && java -jar /app/cmo-pipelines/redcap/redcap_pipeline/target/redcap_pipeline.jar -e -s mskimpact_heme -d .'
            }
        }
    }
}
