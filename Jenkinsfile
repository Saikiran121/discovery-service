pipeline {
    agent any

    tools {
        jdk 'jdk-17'
        maven 'maven-3912'
    }

    stages {
        stage('Check java and mvn version') {
            steps {
                sh '''
                    java --version
                    mvn --version
                '''
            }
        }

        stage('Remove previous builds') {
            steps {
                sh 'mvn clean'
            }
        }

        stage('Compile the Code') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Run test unit') {
            steps {
                sh 'mvn test'
            }
        }
    }
}