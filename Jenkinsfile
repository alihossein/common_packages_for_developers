node {
  stage("build") {
    //checkout scm
    def projects = readJSON file: "/var/jenkins_home/workspace/new3/common_packages_for_developers/json/1.json"
    println(projects)

    def postmanGet = new URL('https://postman-echo.com/post')
    def connectionObject = (HttpURLConnection) postmanGet.openConnection()
    connectionObject.setRequestProperty("Content-Type", "application/json")
    connectionObject.requestMethod = 'POST'
    connectionObject.setDoOutput(true)

    

    if (connectionObject.responseCode == 200) {
      println("[X] send request successfully...")
      println(connectionObject.content.text)
    } else {
      println("[X] can not send request ... try again ...")
      println(connectionObject.content.text)

    }
 

    println("Finish")

  }
}
