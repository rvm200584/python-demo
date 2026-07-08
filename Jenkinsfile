pipeline {
    agent any

    environment {
        IMAGE_NAME = "localhost:5000/python-demo:v1"
    }

    stages {

        stage('Clone') {
            steps {
                git branch: 'main',
                url: 'https://github.com/rvm200584/python-demo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Push') {
            steps {
                sh 'docker push $IMAGE_NAME'
            }
        }

    }
}

