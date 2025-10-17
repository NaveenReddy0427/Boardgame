pipeline {
    agent any
    
    tools {
        maven 'maven3'
        jdk 'jdk17'
    }

    stages {
        stage('git checkout') {
            steps {
               git branch: 'main',url: 'https://github.com/NaveenReddy0427/Boardgame.git'
                echo 'checkout the code'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
               sh 'mvn test'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
