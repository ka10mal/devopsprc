pipeline {
    agent any
    tools{
        maven 'maven-3.9.0'
    }
    stages {
        stage('test') {
            steps {
                echo 'Testing of application'
                sh 'mvn test'
            } 
        }
         stage('build') {
            steps {
                echo 'Building of application'
                sh 'mvn package'
            } 
        }
         stage('deploy') {
            steps {
                echo 'deploying of application'
            } 
        }
    }
}
