node {
  stage("build") {
    checkout scm
    def projects = readJSON file: "/var/jenkins_home/workspace/new3/common_packages_for_developers/json/1.json"
    println(projects)
    
    
    def postmanGet = new URL('https://postman-echo.com/post')
def connectionObject = (HttpURLConnection)postmanGet.openConnection()
connectionObject.setRequestProperty("Content-Type", "application/json")
connectionObject.requestMethod = 'POST'
connectionObject.setDoOutput(true)

String jsonInputString = '{"name": "Upendra", "job": "Programmer"}'
try(OutputStream os = connectionObject.getOutputStream()) {
    byte[] input = jsonInputString.getBytes("utf-8");
    os.write(input, 0, input.length);
}

if (connectionObject.responseCode == 200){
    println("[X] send request successfully...")
    println(connectionObject.content.text)
}else {
    println("[X] can not send request ... try again ...")
    println(connectionObject.content.text)

}
    
    
    
    

    

    // get last commit id
    def res = sh([script: 'git log -n 1 --pretty=format:%H', returnStdout: true]).trim()
    // get which files were changed in last commit 
    def output = sh([script: 'git log ${res} --pretty="format:" --name-only -1', returnStdout: true]).trim()
    
    
 

println("Finish")
    
    
    
     
 
 

  }
}

 
