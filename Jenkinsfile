pipeline {
    agent any 
    stages {
        stage('init') { 
            steps {
                sh '''
                pwd
                cd /var/lib/jenkins/workspace/time
                ls -lart
                terraform init

                '''
            }
        }
        stage('plan') { 
            steps {
              sh '''
              
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