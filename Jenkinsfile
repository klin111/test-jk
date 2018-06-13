pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/home/root/pyshell') {
          git 'https://github.com/klin111/test-jk.git'
        }

        sh 'sudo -H pip -r requirements.txt'
        sh 'python app.py'
      }
    }
  }
}