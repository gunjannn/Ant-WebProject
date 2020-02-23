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

stage('ant build')
{
steps
{
withAnt(installation: 'localAnt', jdk: 'localjdk')
sh "ant -f build.xml -v"
}
}
}
}
