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
        junit(testResults: 'target/surefire-reports/*.xml', allowEmptyResults: true)
      }
    }
  }
}