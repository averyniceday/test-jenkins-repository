pipeline {
    agent {
        docker { image 'cbioportalpipelines/cmo-pipelines:test' 
                 args '-u root' 
               }
    }
    stages {
        stage('Test') {
            steps {
                sh 'cd $CMO_PIPELINES_HOME/redcap && mvn clean install'
            }
        }
    }
}
