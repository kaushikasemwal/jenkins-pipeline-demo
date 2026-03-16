pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                git 'https://github.com/kaushikasemwal/jenkins-pipeline-demo.git
            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
                sh 'mkdir build'
                sh 'echo Build successful'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'echo Tests passed'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                sh 'mkdir deploy'
                sh 'echo Deployment complete'
            }
        }

    }
}
