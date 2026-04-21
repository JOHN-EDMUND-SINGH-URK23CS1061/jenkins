pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/JOHN-EDMUND-SINGH-URK23CS1061/jenkins.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 myapp'
            }
        }
    }
}
