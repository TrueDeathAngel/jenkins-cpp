pipeline {
    agent {
        docker {
            image 'gcc:latest'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o main.exe main.cpp'
            }
        }
        stage('Archive artifact') {
            steps {
                archiveArtifacts artifacts: 'main.exe'
            }
        }
    }
}
