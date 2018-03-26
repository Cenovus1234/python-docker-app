node{
   stage("App Build started"){
      echo 'App build started..'
      git 'https://github.com/padmaavathy/python-docker-app.git'
      }
      
    stage("Docker Build"){
     def app = docker.build "mtanweer/padmavathy"
     }
    
    stage("Tag & Push image"){
       withDockerRegistry([credentialsId: 'DockerID', url: 'https://hub.docker.com']) {
          sh 'docker tag mtanweer/padmavathy manee2k6/padmavathy:008'
          sh 'docker push mtanweer/padmavathy:latest'
          sh 'docker push mtanweer/padmavathy:009'
      }
    }
    
    stage("App deployed"){
     echo 'App deployed to Hub..'
    }


}
