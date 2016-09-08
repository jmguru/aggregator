#!groovy

node {

  stage 'Stage Build'
  this.buildVersion='johng'  
  try {
      assert getOldBuildVersion().matches(getBuildVersion()) : 'Uh oh, some shit failed'
  }
  catch (Err) {
  	echo 'Didn't work, keep going.
  }
  
  stage 'The End, hobo'
}

def getBuildVersion()
{
	return this.buildVersion
}

def getOldBuildVersion() {
	return 'abcde'
}
