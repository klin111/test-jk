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
        git(url: 'https://github.com/klin111/test-jk.git', changelog: true, poll: true)
      }
    }
  }
}