pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                git branch: 'main', url: 'https://github.com/kaushikasemwal/jenkins-pipeline-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building project"
                bat 'mkdir build'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests"
                bat 'echo Tests passed'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying project"
                bat 'mkdir deploy'
            }
        }

    }
}
