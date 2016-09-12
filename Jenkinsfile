


node ('gorgon') {
   
    stage 'Stage Build'
    sh 'chmod 755 ./getServices.sh'
    getSvcs = sh(returnStdout: true, script: './getServices.sh').trim()
    

}

