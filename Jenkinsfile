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
        sh '''
        export JAVA_HOME=/usr/lib/jvm/java-21-openjdk-amd64
        export PATH=$JAVA_HOME/bin:$PATH
        java -version
        javac -version
        mvn clean install
        '''
    }
}

        stage('Deploy') {
            steps {
                echo 'Deploying application'
            }
        }
    }
}
