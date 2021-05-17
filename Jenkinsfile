pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo '[X] Building..'
        echo env.BRANCH_NAME
        echo '[X] Building Finished'
      }
    }
    stage('Test') {
      steps {
        try {
          echo '[X] Testing..'
        }
        catchh (err){
          echo err
        }
      }
    }
    stage('Deploy') {
      steps {
        echo '[X] Deploying....'
      }
    }
  }
}
