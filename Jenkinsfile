node{
   stage("App Build started"){
      echo 'App build started..'
      git ''
      }
      
    stage("Docker Build"){
     def app = docker.build "manee2k6/padmavathy"
    }
    
    stage("Tag & Push image"){
     app.tag "manee2k6/padmavathy:reckon"
     app.push "manee2k6/padmavathy:reckon"
    }
    
    stage("App deployed"){
     echo 'App deployed to Hub..'
    }


}
