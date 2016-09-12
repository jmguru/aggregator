


node ('gorgon') {
   
    stage 'Stage Build'
 
    def svcStr = "sh /var/jenkins_home/getServices.sh".execute().text
    def serviceList = svcStr.tokenize()
    
    println serviceList[0]

}

