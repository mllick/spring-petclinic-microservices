pipeline {
    agent any
    
    tools{
        jdk 'jdk17'
        maven 'maven3'
    }

    stages {
        stage('Git checkout') {
            steps {
                git branch: 'dev', url: 'https://github.com/mllick/spring-petclinic-microservices.git'
            }
        }
        
        stage('Compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        
        stage('Build') {
            steps {
                sh "mvn clean package -DskipTests=true"
            }
        }
        
        
    }
}
