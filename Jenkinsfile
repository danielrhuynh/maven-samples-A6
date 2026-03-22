pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/danielrhuynh/maven-samples-A6.git', branch: 'master')
      }
    }

    stage('bisect') {
      steps {
        sh 'git bisect start <bad-commit-hash> <good-commit-hash>'
        sh 'git bisect run mvn clean test'
      }
    }

  }
  tools {
    maven 'MAVEN'
    jdk 'JDK'
  }
}
