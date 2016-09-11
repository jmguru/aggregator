#!groovy
import groovy.json.JsonSlurper
import groovy.json.JsonBuilder
import groovy.json.JsonOutput
import hudson.FilePath
import hudson.*


node ('gorgon') {
    def projects = []
    projects.add([projectname: 'aggy', ci: true, deployment: false]);
    def json = JsonOutput.toJson(projects)
    println json
    
    hudson.FilePath workspace = hudson.model.Executor.currentExecutor().getCurrentWorkspace()
    
    //new File("${workspace}/test.json").write(new JsonBuilder(projects).toPrettyString())
/*
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
    new File(propPath).write(jsonStr);
*/    
    

}

