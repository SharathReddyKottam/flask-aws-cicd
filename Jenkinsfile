pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest test_app.py -v'
            }
        }

        stage('Dockerize') {
            steps {
                sh 'docker build -t flask-aws-cicd .'
            }
        }

        stage('Run') {
            steps {
                sh 'docker stop flask-aws-cicd || true'
                sh 'docker rm flask-aws-cicd || true'
                sh 'docker run -d -p 5000:5000 --name flask-aws-cicd flask-aws-cicd'
            }
        }
    }
}