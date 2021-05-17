pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        echo env.BRANCH_NAME
        echo 'Building Finished'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}
