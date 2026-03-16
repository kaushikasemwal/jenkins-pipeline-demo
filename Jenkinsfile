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
                echo "Building project..."
                bat 'if not exist build mkdir build'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                bat 'echo Tests passed'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                bat 'if not exist deploy mkdir deploy'
            }
        }

        stage('Job1') {
            steps {
                echo "Creating JOB_1 directory"
                bat 'if not exist JOB_1 mkdir JOB_1'
            }
        }

        stage('Job2') {
            steps {
                echo "Creating JOB_2 inside JOB_1"
                bat 'if not exist JOB_1\\JOB_2 mkdir JOB_1\\JOB_2'
            }
        }

        stage('Job3') {
            steps {
                echo "Creating JOB_3 inside JOB_2"
                bat 'if not exist JOB_1\\JOB_2\\JOB_3 mkdir JOB_1\\JOB_2\\JOB_3'
            }
        }

    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
