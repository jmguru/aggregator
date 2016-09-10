#!groovy

node {

  stage 'Stage Build'
  def slurper = new groovy.json.JsonSlurper();
  def serviceList = readFile('.platform').trim()
  
  println serviceList.dump();
  
}

