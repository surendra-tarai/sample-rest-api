pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage('Test') {
            steps {
                echo 'Application Testing...'
                // sh "python3 api.py"
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploying the application'
                // sh "sudo nohup python3 app.py > log.txt 2>&1 &" 
            }
        }

    }
    post {
        always {
            echo 'the pipeline completed'
        }
        success {
            echo 'API is up and running!'
        }
        failure {
            echo 'Build stage failed'
        }
    }
}
