pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'cat /etc/hosts'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
        sh 'jenkins/test.all.sh'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
        sh 'jenkins/deploy.sh'
      }
    }

  }
}