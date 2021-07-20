pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Stage build'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'Stage test'
        sh 'mvn clean test'
      }
    }

    stage('package') {
      steps {
        echo 'Stage package'
        sh 'mvn package -DskipTests'
        archiveArtifacts 'target/*.war'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
}