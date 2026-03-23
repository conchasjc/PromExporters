pipeline {
    agent { label 'staging' }


    parameters {
        choice(
            name: 'ACTION',
            choices: ['up', 'down', 'maintenance:on', 'maintenance:off', 'restart:grafana', 'restart:prometheus', 'restart:all'],
            description: 'Select which Taskfile action to run'
        )
    }

    stages {
        stage('Select Action') {
            steps {
                echo "Selected Taskfile action: ${params.ACTION}"
                sh "task --version"
            }
        }

        stage('Execute Action') {
            steps {
                echo "Executing Taskfile action..."
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
