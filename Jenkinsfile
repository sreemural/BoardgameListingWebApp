pipeline {
    agent any
    
    tools{
        jdk 'jdk11'
        maven 'maven'
    }

    stages {
        stage('Git-Checkout') {
            steps {
               git 'https://github.com/jaiswaladi2468/BoardgameListingWebApp.git'
            }
        }
        
            stage('Compile') {
            steps {
               sh "mvn clean compile"
            }
        }
        
            stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        
            stage('package') {
            steps {
                sh "mvn package"
            }
        }
        
             stage('install') {
            steps {
                sh "mvn install"
            }
        }
    }
}
