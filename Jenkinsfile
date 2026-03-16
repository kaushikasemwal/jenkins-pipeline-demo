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

        stage('Job1') {
            steps {
                echo "Creating JOB_1 directory"
                bat 'mkdir JOB_1'
            }
        }

        stage('Job2') {
            steps {
                echo "Creating JOB_2 directory inside JOB_1"
                bat 'mkdir JOB_1\\JOB_2'
            }
        }

        stage('Job3') {
            steps {
                echo "Creating JOB_3 directory inside JOB_2"
                bat 'mkdir JOB_1\\JOB_2\\JOB_3'
            }
        }

    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}
