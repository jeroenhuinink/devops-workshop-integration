pipeline {
  agent {
    dockerfile {
      filename 'buildagent/Dockerfile'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'mvn clean verify'
      }
      post {
        always {
          junit(testResults: 'target/surefire-reports/*.xml', allowEmptyResults: true)
        }
      }
    }
  }
}