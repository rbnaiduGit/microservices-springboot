pipeline {
    agent any
    tools {
        maven 'Maven_Home' 
    }
    environment{
        JAVA_HOME="C:/Program Files/Java/jdk-11.0.15"
        
    }
    
    stages {
        stage('install') {
            steps {
                bat "mvn --version"
            }
        }
        stage('git') {
            steps {
                git 'https://github.com/rbnaiduGit/microservices-springboot.git'
            }
        }
        stage('test sh') {
            steps {
               
                   bat "mvn clean test"
              
            }
        }
        
        stage('Build') {
            steps {
               
                   bat "mvn package" 

            }
        }
        
    }
}
