#!groovy

@NonCPS
def jsonParse(def json) {
    return new groovy.json.JsonSlurperClassic().parseText(json);
}
@NonCPS
def jsonBuild(def svcList) {
    return new groovy.json.JsonBuilder(svcList);
}
@NonCPS
def whereAmI() {
    sh 'hostname'
    sh 'pwd'
    return;
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
 
 def builder = jsonBuild(serviceList);
 //builder.content.services[serviceStr].BuildVersion = '1.1';
 //json = builder.toPrettyString();
 //println json
 
 whereAmI();
 //mrFile = new File(propPath);
 //mrFile.delete();
 
  
}

