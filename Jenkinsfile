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
          script {
              if (env.BRANCH_NAME=='master') {
                        stage ('Stage 1') {
                            echo '[X] Test 1 ....'
                        }
                    }
                    if (env.BRANCH_NAME!='master') {
                        stage ('Stage 2') {
                            echo '[X] Test 2 ....'
                        }
                    }
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
