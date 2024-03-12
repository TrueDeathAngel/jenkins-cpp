pipeline {
    agent {
        docker {
            image 'gcc:latest'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o app'
            }
        }
        stage('Archive artifact') {
            steps {
                archiveArtifacts artifacts: 'app'
            }
        }
    }
}
