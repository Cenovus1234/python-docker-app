node{
   stage("App Build started"){
      echo 'App build started..'
      git 'https://github.com/cenovus1234/python-docker-app.git'
      }
      
    stage("Docker Build"){
     def app = docker.build "mtanweer/cenovus1234"
     }
    
    stage("Tag & Push image"){
       withDockerRegistry([credentialsId: 'DockerID', url: 'https://hub.docker.com']) {
          sh 'docker tag cenovus mtanweer/cenovus:1.0'
          sh 'docker push mtanweer/cenovus1234:latest'
          sh 'docker push mtanweer/cenovus1234:009'
      }
    }
    
    stage("App deployed"){
     echo 'App deployed to Hub..'
    }


}
