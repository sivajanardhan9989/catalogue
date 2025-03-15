pipeline {
    agent any
    stages {
        
        stage('Install depdencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Unit test') {
            steps {
                echo "unit testing is done here"
            }
        }
        //sonar-scanner command expect sonar-project.properties should be available
        stage('Sonar Scan') {
            steps {
                sh 'ls -ltr'
                sh 'sonar-scanner'
            }
        }
       
        
        //install pipeline utility steps plugin, if not installed


        //here I need to configure downstram job. I have to pass package version for deployment
        // This job will wait until downstrem job is over
        
    }

    post{
        always{
            echo 'cleaning up workspace'
            //deleteDir()
        }
    }
}