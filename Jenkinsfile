node{
    stage("build"){
        print_some_text("ali")
        println(pwd())
        def res = sh([ script: 'echo 11111111111111111111', returnStdout: true ]).trim()
    }
}

def print_some_text(String my_name){
    echo "welcome ... ${my_name}"
}
