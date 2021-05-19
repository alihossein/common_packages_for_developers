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
                echo 'BRANCH_NAME = ' + env.BRANCH_NAME
                echo 'BRANCH_IS_PRIMARY = ' + env.BRANCH_IS_PRIMARY
                echo 'CHANGE_ID = ' + env.CHANGE_ID
                echo 'CHANGE_URL = ' + env.CHANGE_URL
                echo 'CHANGE_TITLE = ' + env.CHANGE_TITLE
                echo 'CHANGE_AUTHOR = ' + env.CHANGE_AUTHOR
                echo 'CHANGE_AUTHOR_DISPLAY_NAME = ' + env.CHANGE_AUTHOR_DISPLAY_NAME
                echo 'CHANGE_AUTHOR_EMAIL = ' + env.CHANGE_AUTHOR_EMAIL
                echo 'CHANGE_TARGET = ' + env.CHANGE_TARGET
                echo 'Hello World'
            }
    }
  }
}
