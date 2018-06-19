pipeline {
    agent {
        docker { image 'averyniceday/redcap:test' 
                 args '-u root' 
               }
    }
    stages {
        stage('Test') {
            steps {
                sh 'java -jar /app/redcap_pipeline.jar -e -s mskimpact_heme -d .'
            }
        }
    }
}
