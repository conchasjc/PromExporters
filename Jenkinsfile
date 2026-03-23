pipeline {
    agent { label 'staging' }


  

    stages {
        stage('Select Action') {
            steps {
                
                sh "task --version"
            }
        }

        stage('Execute Action') {
            steps {
                echo "Executing Taskfile action..."
                sh "pwd"
                sh "docker ps -a"
            }
        }

        stage('Output Container Status') {
            steps {
                echo 'Showing Container Status'
                sh 'docker ps -a'
            }
        }
    }
}
