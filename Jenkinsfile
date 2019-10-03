pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building....'
                sh 'export JAVA_HOME=/tools/jdk1.8.0_221 && export MAVEN_OPTS="-Xmx3000m" && /usr/local/src/apache-maven/bin/mvn -Dmaven.test.skip=true install'
                sh 'sudo docker build -t aws-demo .'
                sh 'sudo docker images'
                sh 'sudo docker run -p8085:7000 aws-demo'
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
