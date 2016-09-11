#!groovy

node {

  def propPath = '/var/jenkins_home/workspace/build/props.json'
  
  stage 'Stage Build'
  //def slurper = new groovy.json.JsonSlurper();
  def serviceList = readFile(propPath).trim()
  
  println serviceList.dump();
  
}

