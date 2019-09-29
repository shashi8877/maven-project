pipeline
{
   agent any
   



stage "scm checkout"
git 'https://github.com/shashi8877/maven-project.git'
}
}
{

stage ('Testing Stage')


steps{
    withMaven(maven : 'LocalMaven')
    {
      sh 'mvn test'
    }
}


}

}
}
