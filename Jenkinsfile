pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building....'
               // sh 'export JAVA_HOME=/tools/jdk1.8.0_221 && /usr/local/src/apache-maven/bin/mvn ./mvnw'
               sh 'export JAVA_HOME=/tools/jdk1.8.0_221 && ./mvnw'
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
