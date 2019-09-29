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
}
}
