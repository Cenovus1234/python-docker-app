node{
   stage("App Build started"){
      echo 'App build started..'
      git 'https://github.com/Cenovus1234/python-docker-app.git'
      }
      
    stage("Docker Build"){
     def app = docker.build "mtanweer1/padmavathy"
     }
    
    stage("Tag & Push image"){
       withDockerRegistry([credentialsId: 'DockerID', url: 'https://hub.docker.com']) {
          sh 'docker tag mtanweer1/Cenovus1234 mtanweer1/Cenovus1234:008'
          sh 'docker push mtanweer1/Cenovus1234:latest'
          sh 'docker push mtanweer1/Cenovus1234:009'
      }
    }
    
    stage("App deployed"){
     echo 'App deployed to Hub..'
    }


}
