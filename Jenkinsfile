pipeline {
    agent any
    stages {
        stage("Info") {
            steps {
                sh 'docker version'
            }
        }
        stage("Build") {
            agent {
                docker {
                reuseNode true
                image 'gradle:4.7.0-jdk8-alpine'
                }
            }
            steps {
                sh 'gradle --version'
                sh 'gradle build'
            }
        }
    }
}

