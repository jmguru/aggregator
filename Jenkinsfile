


node ('gorgon') {
   
    stage 'Stage Build'
    def serviceList = []
    
    
    def buf = new ByteArrayOutputStream()
    def newOut = new PrintStream(buf)
    def saveOut = System.out
    
    System.out = newOut
    
    System.out = saveOut
    println "sh /var/jenkins_home/getServices.sh".execute().text

    println "TINKY!!! " + buf.toString()

}

