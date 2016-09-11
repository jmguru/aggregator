#!groovy
import groovy.json.*

@NonCPS
def writeFile(def propPath, def jsonStr) {
    new File(propPath).write(jsonStr);
}

node ('gorgon') {
    stage 'Stage Build'
    
    def propPath = '/opt/wl/jenkins/build/props.json';
    def json = readFile(propPath);
    def jsonParse = new groovy.json.JsonSlurperClassic();
    def serviceList = jsonParse.parseText(json);
    def svc = serviceList.services;
    def serviceStr="eventpreprocessor";
  
    println serviceList.services[serviceStr];
    println serviceList.services.keySet();
    json=null;
    
    def builder = new groovy.json.JsonBuilder(serviceList);
    builder.content.services[serviceStr].BuildVersion = '1.1';
    def jsonStr = builder.toPrettyString();
    println jsonStr
    writeFile(propPath, jsonStr)
    

}

