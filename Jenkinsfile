#!groovy

node {

  stage 'Stage Build'
  this.buildVersion='johng'  
  
  assert getOldBuildVersion().matches(getBuildVersion()) : "AAAw shit!"
  
  stage 'The End, hobo'
}

def getBuildVersion()
{
	return this.buildVersion
}

def getOldBuildVersion() {
	return 'abcde'
}
