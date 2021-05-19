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
                echo 'CHANGE_FORK = ' + env.CHANGE_FORK
                echo 'TAG_NAME = ' + env.TAG_NAME
                echo 'TAG_TIMESTAMP = ' + env.TAG_TIMESTAMP
                echo 'TAG_UNIXTIME = ' + env.TAG_UNIXTIME
                echo 'TAG_DATE = ' + env.TAG_DATE
                echo 'BUILD_NUMBER = ' + env.BUILD_NUMBER
                echo 'BUILD_ID = ' + env.BUILD_ID
                echo 'BUILD_DISPLAY_NAME = ' + env.BUILD_DISPLAY_NAME
                echo 'JOB_NAME = ' + env.JOB_NAME
                echo 'JOB_BASE_NAME = ' + env.JOB_BASE_NAME
                echo 'BUILD_TAG = ' + env.BUILD_TAG
                echo 'EXECUTOR_NUMBER = ' + env.EXECUTOR_NUMBER
                echo 'NODE_NAME = ' + env.NODE_NAME
                echo 'NODE_LABELS = ' + env.NODE_LABELS
                echo 'WORKSPACE = ' + env.WORKSPACE
                echo 'WORKSPACE_TMP = ' + env.WORKSPACE_TMP
                echo 'JENKINS_HOME = ' + env.JENKINS_HOME
                echo 'JENKINS_URL = ' + env.JENKINS_URL
                echo 'BUILD_URL = ' + env.BUILD_URL
                echo 'JOB_URL = ' + env.JOB_URL
                echo 'Hello World'
            }
    }
  }
}
