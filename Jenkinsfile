node {
  stage("build") {
   checkout scm
    
    
    // Get last commit_id
    def res = sh([ script: 'git log -n 1 --pretty=format:%H', returnStdout: true ]).trim()
    // list all the files in a commit
    def output= sh([ script: 'git log ${res1} --pretty="format:" --name-only -1', returnStdout: true ]).trim()
    
    // Convert String value to list
    String[] str
    files_list = output.split(' ');
    
    // Check each file and send a new request If the file is valid
     for (String file_name in files_list) {
        println("File name is :  $file_name ")
        if (file_name.startsWith("Druid/Ingestion")) {
           send_request_to_druid("/var/jenkins_home/workspace/new3/common_packages_for_developers/json/1.json")
        } else {
          println("This file ( $file_name )  is not available in the druid directory")
           
        }
    }
    
    
   
    
   
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
