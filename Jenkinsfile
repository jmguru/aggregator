#!groovy

node {

  stage 'Stage Build'
  this.buildVersion='johng'  

  assert getOldBuildVersion().matches(getBuildVersion()) : 'Uh oh, some shit failed'
  stage 'The End, hobo'
}

def getBuildVersion()
{
	return this.buildVersion
}

def getOldBuildVersion() {
	return 'abcde'
}
