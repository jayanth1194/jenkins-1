pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "stage1"
                sh '''
                 pwd
                 ls -lart
                 mkdir jayant

                '''
            }
        }
        stage('Test') { 
            steps {
                echo "stage2"
            }
        }
        stage('Deploy') { 
            steps {
                echo "stage3"
            }
        }
    }
    post {
        always{
            echo "after stage only, it will work"
        }
        success{
            echo "it will for sucess"
        }
        failure {
            echo " it will work for failure"
        }
    }
}