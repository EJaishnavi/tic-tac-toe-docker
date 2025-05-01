pipeline{
agent any
 stages{
   stage("docker build & push")
  {
    steps{
      script{
        
        sh 'docker build -t toeimage .'
       
}
        
      }
   }
  stage("docker push")
  {
   steps{
    script{
     withDockerRegistry(credentialsId: 'docker-pswd') 
     {
     sh 'docker tag toeimage jaishnavi08/gameimage:v1'
     sh 'docker push jaishnavi08/gameimage:v1'
     }
}
    }
   }
  }
}
 
 
