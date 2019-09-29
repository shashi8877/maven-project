pipeline {
	agent any
	
	
	stages
	{
		stage ("scm checkout")
		{
git 'https://github.com/shashi8877/maven-project.git'		}
		}
   {
   
stage ('Test stage'){

steps {
withMaven(maven: 'LOCAL MAVEN') 
{
   sh 'mvn test'
}
}
}
}

 {
   
stage ('create package'){

steps {
withMaven(maven: 'LOCAL MAVEN') 
{
   sh 'mvn package'
}
}
}
}
 {
   
stage ('Install package'){

steps {
withMaven(maven: 'LOCAL MAVEN') 
{
   sh 'mvn install'
}
}
}
	 stage ('deploy to tomcat'){

steps {
	sshagent(['172.31.24.146']) {
	sh 'scp -o StrictHostKeyChecking=no **/*.war ec2-user@172.31.24.146:/var/lib/tomcat/webapps'
	}
}	
}

