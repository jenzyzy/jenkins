pipeline {
    agent dev

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
              echo 'cloning done'
            }
        }
        stage('Build') {
            steps {
               echo 'bulid done'
            }
        }
        stage('demo') {
            steps {
                echo "done"
            }
        }
    }
}
