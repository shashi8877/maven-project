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
withMaven(maven: 'Maven_3_6_3') 
{
   sh 'mvn test'
}
}
}
}

 {
   
stage ('create package'){

steps {
withMaven(maven: 'Maven_3_6_3') 
{
   sh 'mvn package'
}
}
}
}
 {
   
stage ('Install package'){

steps {
withMaven(maven: 'Maven_3_6_3') 
{
   sh 'mvn install'
}
}
}
	 stage ('deploy to tomcat'){

steps {
	sshagent (['35.194.61.169']) {
	sh 'scp -o StrictHostKeyChecking=no */target/*.war ubuntu@35.194.61.169:/var/lib/tomcat/webapps'
	}
}	
}
 }
}
