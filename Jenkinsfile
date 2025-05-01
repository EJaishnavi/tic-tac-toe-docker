pipeline{
agent any
 stages{
   stage("docker build & push")
  {
    steps{
      scripts{
        withDockerRegistry(credentialsId: 'docker-pswd') {
        sh 'docker build -t toeimage .'
        sh "docker tag toeimage jaishnavi08/gameimage:v1"
        sh "docker push jaishnavi08/gameimage:v1"
}
        
      }
   }
}
 
 }
}
