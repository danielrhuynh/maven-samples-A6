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

    stage('bisect') {
      steps {
        sh `git bisect start <bad-hash> <good-hash>`
        sh `git bisect run mvn test`
      }
    }

  }
  tools {
    maven 'MAVEN'
    jdk 'JDK'
  }
}
