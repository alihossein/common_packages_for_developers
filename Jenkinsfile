node {
  stage("build") {
    //checkout scm
    def aa = readJSON file: "/var/jenkins_home/workspace/new3/common_packages_for_developers/json/1.json"
    println(aa)

    def postmanGet = new URL('http://10.10.0.44:8888/druid/indexer/v1/task')
    def connectionObject = (HttpURLConnection) postmanGet.openConnection()
    connectionObject.setRequestProperty("Content-Type", "application/json")
    connectionObject.requestMethod = 'POST'
    connectionObject.setDoOutput(true)
    
    String jsonInputString1 = '{"name": "Upendra", "job": "Programmer"}'
    println(jsonInputString1)
    
    
    String jsonInputString = aa
    OutputStream os = connectionObject.getOutputStream()
        byte[] input = jsonInputString.getBytes("utf-8");
        os.write(input, 0, input.length);
    

    

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
