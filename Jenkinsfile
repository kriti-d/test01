pipeline {
  agent any
  stages {
    stage('snyk') {
      steps {
        snykSecurity(failOnIssues: true, monitorProjectOnBuild: true, targetFile: 'results.html', snykInstallation: 'SNYKv2Test')
      }
    }
  }
}
