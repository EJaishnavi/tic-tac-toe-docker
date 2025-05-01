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
 stage("deploy to container")
   {
     steps{
      sh 'docker run -d --name mygame -p 8080:8081 jaishnavi08/gameimage:v1'
     }
   }
 }
}
