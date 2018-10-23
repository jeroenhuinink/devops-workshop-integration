pipeline {
  agent {
    docker {
      image 'maven'
    }

  }
  stages {
    stage('error') {
      steps {
        tool(name: 'Latest', type: 'maven')
        sh 'mvn clean verify'
      }
    }
  }
}