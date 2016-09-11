#!groovy
import groovy.json.*

/*
@NonCPS
def jsonParse(def json) {
    return new groovy.json.JsonSlurperClassic().parseText(json);
}
*/

node ('gorgon') {
    stage 'Stage Build'
    
    def propPath = '/opt/wl/jenkins/build/props.json';
    def json = readFile(propPath);
    def jsonParse = new groovy.json.JsonSlurperClassic();
   // def serviceList = jsonParse.parseText(readFile(propPath));

/*
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
  */
}

