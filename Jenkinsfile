


node ('gorgon') {
   
    stage 'Stage Build'
    def serviceList = []
    
    
    def buf = new ByteArrayOutputStream()
    def newOut = new PrintStream(buf)
    def saveOut = System.out

    System.out = newOut;
    
println "redirected call\n---------------"
System.out = newOut
println "sh /var/jenkins_home/getServices.sh".execute().text
System.out = saveOut

println buf.toString()

}

