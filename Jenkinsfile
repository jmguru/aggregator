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
  
  println serviceList.services.$(serviceStr);
  
  // Important, don't forget this! 
  //println serviceList.services.keySet();
  
}

