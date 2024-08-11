pipeline {
    agent any
    tools{
        jdk 'jdk17'
        maven 'maven'
        
    }
    stages {
        stage('SCM') {
            steps {
            git branch: 'main', credentialsId: 'gitcred', url: 'https://github.com/Navya72075/javawar.git'    
            }
        }
        stage('VALIDATE') {
            steps {
            sh "mvn validate"    
            }
        }
        stage('COMPILE') {
            steps {
            sh "mvn compile"    
            }
        }
        stage('TEST') {
            steps {
            sh "mvn test"    
            }
        }
        stage('PACKAGE') {
            steps {
            sh "mvn package"    
            }
        }
        stage('VERIFY') {
            steps {
            sh "mvn verify"    
            }
        }
        stage('INSTALL') {
            steps {
            sh "mvn install"    
            }
        }
    }
}
