#!groovy
import groovy.json.*

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
    json = builder.toPrettyString();
    println json
    new File(propPath).write(json);
    
/*
  
  
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

