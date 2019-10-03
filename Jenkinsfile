pipeline {
    agent any

    stages {
        stage('Maven Build') {
            steps {
                echo 'Building....'
                sh 'pwd'
                sh 'export JAVA_HOME=/tools/jdk1.8.0_221 && export MAVEN_OPTS="-Xmx3000m" && /usr/local/src/apache-maven/bin/mvn -Dmaven.test.skip=true install'
                sh 'ls'
            }
        }
        stage('Docker Build') {
            steps {
                echo 'Docker Build'
                
               sh ' docker build -t aws/test .'
              sh 'sudo docker images'
                sh 'sudo docker run -p8085:7000 aws/test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
