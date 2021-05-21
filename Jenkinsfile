node {
  stage("build") {
    checkout scm
    print_some_text("ali")
    println(pwd())
    dir('/var/jenkins_home') {
      println(pwd())
    }

    // get last commit id
    def res = sh([script: 'git log -n 1 --pretty=format:%H', returnStdout: true]).trim()
    // get which files were changed in last commit 
    def output = sh([script: 'git log ${res} --pretty="format:" --name-only -1', returnStdout: true]).trim()
    
    
    def postmanGet = new URL('https://postman-echo.com/get')
def getConnection = postmanGet.openConnection()
getConnection.requestMethod = 'GET'
if (getConnection.responseCode == 201){
    println("[X] send request successfully...")
}else {
    println("[X] can not send request ... try again ...")

}

println("Finish")
    
    
    
     

    String[] files_list
    files_list = output.split(' ');

    for (int file_name in files_list) {
      if (file_name.startsWith("json")) {
        println("okkkkkkkkkkkkkkkkkkkkkkkkkkkk")
      } else {
        println("noooooooooooooooooooooooo")
      }
    }

  }
}

def print_some_text(String my_name) {
  echo "welcome ... ${my_name}"
}
