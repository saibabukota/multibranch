node{
{
try
{
stage'select the build type'
if (env.BRANCH_NAME == 'develop')
{
print "Building the develop branch "
//calling the function developBranch if develop branch is getting built
developBranch()
}
else if (env.BRANCH_NAME == 'master')
{
print "Building the master branch "
//calling the function masterBranch if master branch is getting built
masterBranch()
}
else
{
print "Building the feature branch"
//calling the function featureBranch if feature branch is getting built
featureBranch()
}
}
catch(e)
{
currentBuild.result = "FAILED"
throw(e)
}
finally
{
notifyBuild(currentBuild.result)
}
}
