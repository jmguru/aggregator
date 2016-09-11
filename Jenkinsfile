#!groovy

@NonCPS
def jsonParse(def json) {
    return new groovy.json.JsonSlurperClassic().parseText(json);
}


node ('gorgon') {

  def propPath = '/opt/wl/jenkins/build/props.json'
  
  stage 'Stage Build'
  def serviceList;
  
  serviceList = jsonParse(readFile(propPath));
  
  def services= serviceList.services;
  
  def serviceStr="eventpreprocessor";
  
  println serviceList.services[serviceStr];
  
  println serviceList.services.keySet();
  
  //Update
  sh 'hostname; pwd'
  def builder = new groovy.json.JsonBuilder(serviceList);
  sh 'hostname; pwd'
  builder.content.services[serviceStr].BuildVersion = '1.1';
  json = builder.toPrettyString();
  println json
  
  //new File(propPath).write(json);
  
}

