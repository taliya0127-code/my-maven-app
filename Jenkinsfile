pipeline {
    agent any

    tools {
        jdk 'jdk-17'
        maven 'maven-3.9.9'
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/taliya0127-code/my-maven-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}