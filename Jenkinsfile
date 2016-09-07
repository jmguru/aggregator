#!groovy

node {

  stage 'Stage Build'

  // branch name from Jenkins environment variables
  echo "My branch is: ${env.BRANCH_NAME}
  
  def flavor = flavor(env.BRANCH_NAME)
  echo "Building flavor ${flavor}"
  

}

@NonCPS
def flavor(branchName) {
  def matcher = (env.BRANCH_NAME =~ /([a-z_]+)/)
  assert matcher.matches()
  matcher[0][1]
}
