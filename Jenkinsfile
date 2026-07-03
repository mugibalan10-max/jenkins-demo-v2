pipeline {
  agent any

  tols {
    jdk 'JDK17'
  }

  stages {
    stage('Build') {
      steps {
        sh 'java -version'
        sh 'mvn -version'
        sh 'mvn clean package'
      }
    }
  }
  post {
    success {
      echo 'Build Successful!'
    }
    failure {
      echo 'Build Failed!'
    }
  }
}
