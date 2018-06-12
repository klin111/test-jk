pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/home/leo/test-git') {
          git(changelog: true, url: 'https://github.com/klin111/test-jk', poll: true)
        }

      }
    }
  }
}