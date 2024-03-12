pipeline {
    agent {
        docker {
            image 'gcc:latest'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o app main.cpp'
            }
        }
        stage('Archive artifact') {
            steps {
                archiveArtifacts artifacts: 'app'
            }
        }
    }
}
