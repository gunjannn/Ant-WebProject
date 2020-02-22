pipeline
{
agent any
stages
{
stage
{
  steps('scm checkout')
  {
    git branch: 'master', url: "https://github.com/gunjannn/Ant-WebProject"
 }
 }

stage
{
steps('deploy to tomcat')
{
withAnt(jdk: 'localjdk') 
{
   sshagent (['tomcat']) 
	 {
     sh 'scp -o StrictHostKeyChecking=no */target/*.war ec2-user@172.31.92.121:/usr/share/tomcat/webapps/'
    }
 }
}
}
}
