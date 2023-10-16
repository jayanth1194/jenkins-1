pipeline {
    agent any 
    options {
        ansiColor('xterm')
    }
    stages {
        stage('init') { 
            steps {
                sh '''
                pwd
                
                ls -lart
                terraform init

                '''
            }
        }
        stage('plan') { 
            steps {
              sh '''
              pwd
               terraform plan
               '''
            }
        }
        stage('Apply') { 
            steps {
                sh '''
             
                terraform apply '''
            }
        }
    }

    
    post {
       
        success{
            echo "it will for sucess"
        }
        failure {
            echo " it will work for failure"
        }
    }
}