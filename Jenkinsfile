node{
    stage("build"){
        print_some_text("ali")
        println(pwd())
        dir('/var/jenkins_home'){
         println(pwd())   
        }
        def res = sh([ script: 'date', returnStdout: true ]).trim()
        println(res)
        
    }
}

def print_some_text(String my_name){
    echo "welcome ... ${my_name}"
}
