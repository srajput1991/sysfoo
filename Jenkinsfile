pipeline {
  agent any

  tools { maven 'Maven 3.6.1'}

  stages {
    stage('Build'){
      steps {
        echo 'Stage build'
        sh 'mvn compile'
      }
    }
    stage('test'){
      steps {
        echo 'Stage test'
        sh 'mvn clean test'
      }
    }
    stage('Build'){
      steps {
        echo 'Stage package'
        sh 'mvn package -DskipTests'
      }
    }
  }
}
