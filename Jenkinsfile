#!groovy

node {

  stage 'Stage Build'
  def slurper = new groovy.json.JsonSlurper();
  def serviceList
  
  java.nio.file.Paths.get('resources/report.json').withReader { reader ->
     serviceList = slurper.parse(reader)
  }
  
  println serviceList.dump();
  
}

