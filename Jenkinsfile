pipeline {
  agent any
  stages {
    stage('Compile') {
      agent any
      steps {
        sh './gradlew compileJava'
      }
    }

    stage('Unit test') {
      agent any
      steps {
        sh './gradlew test'
      }
    }

  }
}