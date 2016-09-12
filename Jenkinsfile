#!groovy
import groovy.json.JsonSlurper
import groovy.json.JsonBuilder
import groovy.json.JsonOutput
import hudson.FilePath
import hudson.*


node ('gorgon') {
   
    stage 'Stage Build'
    sh 'chmod 755 ./getServices.sh'
    getSvcs = sh(returnStdout: true, script: 'getServices.sh').trim()
    

}

