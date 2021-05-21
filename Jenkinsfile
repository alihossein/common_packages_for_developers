node {
  stage("build") {
    checkout scm
    def projects = readJSON file: "/var/jenkins_home/workspace/new3/common_packages_for_developers/json/1.json""

    

    // get last commit id
    def res = sh([script: 'git log -n 1 --pretty=format:%H', returnStdout: true]).trim()
    // get which files were changed in last commit 
    def output = sh([script: 'git log ${res} --pretty="format:" --name-only -1', returnStdout: true]).trim()
    
    
 

println("Finish")
    
    
    
     
 
 

  }
}

 
