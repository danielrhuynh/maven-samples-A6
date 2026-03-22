pipeline {
  agent any
  tools { 
      maven 'MAVEN' 
      jdk 'JDK' 
  }
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
}
