pipeline {
    agent any
    tools {
        maven 'maven-3'
    }
}

stage {
    stage('Build and Deploy'){
        steps {
            sh 'mvn clean package'
            sh 'java -jar /target/*.jar &'
        }
    }
}
