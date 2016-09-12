
/* TDOs
 * 1) Install and configure slave setup plugin
 * 2) You learned that DSL groovy calls are done on the master. Default directory is /, so need to spec. absolute paths.
 * 2) Copy jq binary into your slave setup files directory.
 * 3) Change your getServices.sh and code in Jenkinsfile to specify absolute path: /var/jenkins_home/... 
*/

node ('gorgon') {
   
    stage 'Stage Build'
    
    def boom = sh script: 'sh getServices.sh', returnStdout: true
    boomlist = boom.tokenize();
    print boomlist[1]; 

}

