pipeline {
    agent any

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
            } 
        }
         stage('deploy') {
            steps {
                echo 'deploying of application'
            } 
        }
    }
}
