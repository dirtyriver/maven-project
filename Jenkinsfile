pipeline {
    agent any
    tools {
        maven 'Default'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
                sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        }
    }
}
