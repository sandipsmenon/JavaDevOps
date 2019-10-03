pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building....'
                sh 'echo $JAVA_HOME'
                sh '/usr/local/src/apache-maven/bin/mvn spring-boot:run'
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
