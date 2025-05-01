pipeline{
agent any
 stages{
   stage("docker build & push")
  {
    steps{
      script{
        withDockerRegistry(credentialsId: 'docker-pswd') {
        sh 'docker build -t toeimage .'
       
}
        
      }
   }
}
 
 }
}
