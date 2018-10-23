pipeline {
  agent {
    docker {
      image 'maven'
    }

  }
  stages {
    stage('build') {
      steps {
        tool(name: 'Latest', type: 'maven')
        sh 'mvn clean verify'
      }
    }
  }
}