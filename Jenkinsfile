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
        // stage('Sonar Scan') {
        //     steps {
        //         sh 'ls -ltr'
        //         sh 'sonar-scanner'
        //     }
        // }

        stage('Build') {
            steps {
                echo "building the code"
                sh 'ls -ltr'
                sh 'zip -r ./* --exclude=.git --exclude=.zip'
            }
        }

        

       
        
        stage('deploy') {
            steps {
                echo "deploying the code"
            }
        }
        //install pipeline utility steps plugin, if not installed


        //here I need to configure downstram job. I have to pass package version for deployment
        // This job will wait until downstrem job is over
        
    }

    post{
        always{
            echo 'cleaning up workspace'
            // deleteDir()
        }
    }
}