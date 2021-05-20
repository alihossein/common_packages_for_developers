node {
  stage("build") {
    checkout scm
    print_some_text("ali")
    println(pwd())
    dir('/var/jenkins_home') {
      println(pwd())
    }

    def res = sh([script: 'git rev-parse HEAD', returnStdout: true]).trim()
    println(res)
    def res1 = sh([script: 'git log -n 1 --pretty=format:%H', returnStdout: true]).trim()
    println(res1)
    def output = sh([script: 'git log ${res1} --pretty="format:" --name-only -1', returnStdout: true]).trim()
    println(output)

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
