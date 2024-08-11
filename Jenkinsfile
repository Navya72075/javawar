pipeline {
    agent any
    tools{
        jdk 'jdk17'
        maven 'maven'
        
    }
    stages {
        stage('SCM') {
            steps {
            git 'https://github.com/RavitejaAdepudi/javawar.git'    
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
