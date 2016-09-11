#!groovy

@NonCPS
def jsonParse(def json) {
    new groovy.json.JsonSlurperClassic().parseText(json)
}

node ('gorgon') {

  def propPath = '/opt/wl/test/workspace/build/props.json'
  
  stage 'Stage Build'
  def serviceList = readFile(propPath).trim()
  
  jsonParse(serviceList);
  
  println serviceList.dump();
  
}

