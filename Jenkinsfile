


node ('gorgon') {
   
    stage 'Stage Build'
    def serviceList = []
    
    def services = "sh /var/jenkins_home/getServices.sh".execute().text

    def l = Eval.me(services)

    println l[0]

}

