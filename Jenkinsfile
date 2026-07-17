pipeline {
    agent any

    stages {

        stage('Build Maven') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t hello-world .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run --rm hello-world'
            }
        }
    }
}
