pipeline {
  agent any

  stages {
    stage('Build') {
      if (env.BRANCH_NAME == "develop") {
        echo '[X] this is a develop branch.'
      } else {
        echo '[X] this is a another branch.'

      }
      steps {
        echo 'Building..'
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
