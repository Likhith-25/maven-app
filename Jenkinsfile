pipeline{
    agent any
    tools{
        maven 'Maven'
    }
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
                sh 'docker run -p 8081:8081 maven-external'
            }
        }
    }
}
