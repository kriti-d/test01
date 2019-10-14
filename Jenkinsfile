pipeline {
  agent {
    docker {
      image 'node:8'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'sh \'npm install\''
      }
    }
    stage('snyk') {
      steps {
        snykSecurity(failOnIssues: true, monitorProjectOnBuild: true, targetFile: 'results.html', snykInstallation: 'SNYKv2Test')
      }
    }
  }
}