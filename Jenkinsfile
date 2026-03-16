pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                git 'https://github.com/kaushikasemwal/jenkins-pipeline-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building project..."
                sh 'mkdir build'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'echo Tests successful'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying project..."
                sh 'mkdir deploy'
            }
        }

    }
}
