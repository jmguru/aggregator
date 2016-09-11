#!groovy

@NonCPS
def jsonParse(def json) {
    return new groovy.json.JsonSlurperClassic().parseText(json);
}


node ('gorgon') {

  def propPath = '/opt/wl/test/workspace/build/props.json'
  
  stage 'Stage Build'
  def serviceList = [];
  
  serviceList = jsonParse(readFile(propPath));
 
  def services= serviceList.services;
  
  def serviceStr="eventpreprocessor";
  
  println serviceList.services[serviceStr];
  
  println serviceList.services.keySet();
  
  //Update
 
 //def builder = new groovy.json.JsonBuilder(serviceList);
 //builder.content.services[serviceStr].BuildVersion = '1.1';
 //json = builder.toPrettyString();
 //println json
 
 node ('gorgon') {
    sh 'pwd'
    sh 'hostname'
    println propPath
    mrFile = new File(propPath);
    mrFile.delete();
 }
  
}

