pipeline {
  agent any
  stages {
    
    stage('compile') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps{
        sh 'mvn test'
      }
    }

    stage('build') {
      steps {
        sh 'mvn clean package'
      }
      
    }
  }
    post {
      success {
        echo 'build is success'
      }
      failure {
        echo 'build is failure'
      }
      always {
        echo 'build completed'
      }
    }
}

