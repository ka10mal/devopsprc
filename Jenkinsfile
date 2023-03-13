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
                withcredentials([usernamePassword( credentialId: 'docker' , usernameVariable:'USERNAME' , passwordVariable:'PAASWORD')])
                sh 'docker build -t ka10mal/spring_boot:1.0 .'
                sh "docker login -u $USERNAME -p $PASSWORD"
                sh 'docker push ka10mal/spring_boot:1.0'
            } 
        }
    }
}
