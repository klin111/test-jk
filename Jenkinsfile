pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      agent {
        node {
          label 'dev'
        }

      }
      steps {
        dir(path: '/root/jenkins')
        git(url: 'https://github.com/klin111/test-jk.git', changelog: true, poll: true)
      }
    }
    stage('build') {
      agent {
        node {
          label 'dev'
        }

      }
      steps {
        sh 'sudo -H pip install -r requirements.txt'
      }
    }
    stage('run') {
      agent {
        node {
          label 'dev'
        }

      }
      steps {
        sh 'python app.py'
      }
    }
  }
}