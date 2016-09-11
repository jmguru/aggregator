#!groovy

@NonCPS
def jsonParse(def json) {
    return new groovy.json.JsonSlurperClassic().parseText(json);
}

node ('gorgon') {

  def propPath = '/opt/wl/test/workspace/build/props.json'
  
  stage 'Stage Build'
  def serviceList = jsonParse(readFile(propPath));
 
  println serviceList.eventpreprocessor;
  
}

