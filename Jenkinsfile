pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/danielrhuynh/maven-samples-A6.git', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'mvn verify'
      }
    }

  }
  tools {
    maven 'MAVEN'
    jdk 'JDK'
  }
}