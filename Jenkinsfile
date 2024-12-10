pipeline {
    agent any
    tools { 
        jdk 'jdk-21' 
    }
    environment { 
        JAVA_HOME = 'C:\\Program Files\\Java\\jdk-21' 
    }
    stages {
        stage('Compile Stage') {
            steps {
                withMaven(maven: 'Maven-3.9.9') {
                    bat 'mvn clean compile'
                }
            }
        }
        stage('Testing Stage') {
            steps {
                withMaven(maven: 'Maven-3.9.9') {
                    bat 'mvn test'
                }
            }
        }
        stage('Install Stage') {
            steps {
                withMaven(maven: 'Maven-3.9.9') {
                    bat 'mvn install'
                }
            }
        }
    }
}
