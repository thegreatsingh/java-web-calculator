pipeline {
    agent any

    tools {
        maven 'maven-3'
    }

    stages {

        stage('Build and Deploy') {
            steps {
                sh 'mvn clean package'
                sh 'java -jar target/*.jar &'
            }
        }

    }
}
