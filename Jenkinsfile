pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building....'
                sh 'export JAVA_HOME=/tools/jdk1.8.0_221 && /usr/local/src/apache-maven/bin/mvn install'
                sh 'docker build -t "aws-demo" .'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
