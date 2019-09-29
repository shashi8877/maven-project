pipeline
{
   agent any
   



   stages
   {
      stage ("scm checkout"){
      git 'https://github.com/shashi8877/maven-project.git'
}
}

   {

stage ('Testing Stage')
   {


steps
      {
    withMaven(maven: 'LOCAL MAVEN')
    {
      sh 'mvn test'
    }
}

}
   }
}
   }
}
}





