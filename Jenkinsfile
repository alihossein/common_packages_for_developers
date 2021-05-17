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
       if (env.BRANCH_NAME=='master'){
           echo '[X] Test 1 ....'
       }else
       {
           echo '[X] Test 2 ....'

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
