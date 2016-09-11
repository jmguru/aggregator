#!groovy

@NonCPS
def jsonParse(def json) {
    new groovy.json.JsonSlurperClassic().parseText(json)
    return new HashMap<>(slurper.parseText(json))
}

node ('gorgon') {

  def propPath = '/opt/wl/test/workspace/build/props.json'
  
  stage 'Stage Build'
  def serviceList = jsonParse(readFile(propPath));
 
  println serviceList.dump();
  
}

