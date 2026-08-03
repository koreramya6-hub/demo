pipeline {
    agent any

    stages {

        stage('Check Java') {
            steps {
                sh 'which java'
                sh 'which javac'
                sh 'echo $JAVA_HOME'
                sh 'java -version'
                sh 'javac -version'
                sh 'mvn -version'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application'
            }
        }
    }
}
