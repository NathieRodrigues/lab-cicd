pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'mvn -B -DskipTests clean package'
          }
        }

        stage('test') {
          steps {
            sleep 3
          }
        }

      }
    }

  }
  tools {
    maven 'maven-3.6.3'
    jdk 'jdk-8'
  }
}