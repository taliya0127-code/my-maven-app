pipeline {
    agent any

    tools {
        jdk 'jdk-17'
        maven 'Maven-3.9.9'
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/taliya0127-code/my-maven-app.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}