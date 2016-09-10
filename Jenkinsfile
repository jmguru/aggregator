#!groovy

import groovy.json.slurper
import java.nio.file.Paths

node {

  stage 'Stage Build'
  JsonSlurper slurper = new JsonSlurper();
  def serviceList
  
  Paths.get('resources/report.json').withReader { reader ->
    serviceList = slurper.parse(reader)
  }
  
  println serviceList.dump();
  
}

