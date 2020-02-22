pipeline
{
agent any
stages
{
stage('scm checkout')
{
  steps
  {
    git branch: 'master', url: "https://github.com/gunjannn/Ant-WebProject"
 }
 }

stage('deploy to tomcat')
{
steps
{
withAnt(installation: 'LocalAnt')
sh "ant build"
}
}
}
}
}
