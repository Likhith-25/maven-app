pipeline{
    agent any
    stages{
       stage('build'){
            steps{
                sh ' mvn clean package'
            }
        }
        stage('docker'){
            steps{
                sh 'docker build -t maven-external .'
            }
        }
        stage('run'){
            steps{
                sh 'docker run maven-external'
            }
        }
    }
}
