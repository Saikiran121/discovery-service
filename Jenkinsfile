pipeline {
    agent any

    stages {
        stage('Check java and mvn version') {
            steps {
                sh '''
                    java --version
                    mvn --version
                '''
            }
        }
    }
}