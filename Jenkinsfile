pipeline {
    agent any

    tools {
  maven 'mevan'
}

    stages {
        stage('git clone') {
            steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/jenzyzy/jenkins.git']])
            }
        }
        stage('test') {
            steps {
              sh 'mvn test'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn package'
                sh 'echo "this build ${BUILD_NUMBER}"'
            }
        }
        stage('demo') {
            steps {
                echo "done"
            }
        }
    }
}
