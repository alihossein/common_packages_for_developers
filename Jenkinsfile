node {
  stage("build") {
    //checkout scm
    
    send_request_to_druid("/var/jenkins_home/workspace/new3/common_packages_for_developers/json/1.json")
    
   
    println("Finish")

  }
}

def send_request_to_druid(String file_name){
  
  // Create a URL object
    def urlObject = new URL('http://10.10.0.44:8888/druid/indexer/v1/task')
    //Open a Connection .  this method only creates a connection object but doesn't establish the connection yet.
    def connectionObject = urlObject.openConnection()
    //Set the Request Method
    connectionObject.requestMethod = 'POST'
    //Set all of your needed headers
    connectionObject.setRequestProperty("Content-Type", "application/json");
    // Ensure the Connection Will Be Used to Send Content
    connectionObject.setDoOutput(true);
    // Setting the connect and read timeouts.
    connectionObject.setConnectTimeout(5000)
    connectionObject.setReadTimeout(5000)
    

    def myFile = new File(file_name)
    String jsonInputString=myFile.text

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
}
