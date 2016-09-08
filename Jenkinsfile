#!groovy

node {

  stage 'Stage Build'
  this.buildVersion='7.1.2'  
  
  try {
    assert this.buildVersion == '6.15.8' : "you suck chigger"
  }
  catch(Err) {
    echo "Nevermind! "  
  }
  
  stage 'The End, hobo'
}

