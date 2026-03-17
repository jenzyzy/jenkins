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
              sh 'mvn clean'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn package'
               
            }
        }
        stage('demo') {
            steps {
                echo "done"
            }
        }
    }
}
