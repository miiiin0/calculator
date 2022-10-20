pipeline {
  agent any
  stages {
    stage('Compile') {
      agent any
      steps {
        sh '''pipeline {
   agent any

   stages {
     stage("Compile") {
        steps {
           sh "./gradlew compileJava"
        }
     }

     stage("Unit test"){
        steps {
           sh "./gradlew test"
        }
     }
   }
}'''
        }
      }

      stage('Unit test') {
        agent any
        steps {
          sh '''pipeline {
   agent any

   stages {
     stage("Compile") {
        steps {
           sh "./gradlew compileJava"
        }
     }

     stage("Unit test"){
        steps {
           sh "./gradlew test"
        }
     }
   }
}'''
          }
        }

      }
    }