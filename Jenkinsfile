pipeline {
    agent any

    tools {
        maven 'maven-3'
    }

    stages {

        stage('Build') {
            steps {
                sh 'mvn clean package'
            
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarServer') {
                    sh 'mvn clean verify sonar:sonar'
                }
            }
    }
        stage('Deploy') {
            steps {
                sh 'java -jar target/*.jar &'
            }
        }

    }
}
