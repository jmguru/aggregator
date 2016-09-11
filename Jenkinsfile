#!groovy

node {

  stage 'Stage Build'
  def slurper = new groovy.json.JsonSlurper();
  def serviceList = readFile('build/props.json').trim()
  
  println serviceList.dump();
  
}

