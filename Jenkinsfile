
pipeline {

  agent any 

  stages {

    stage("frontend"){
      steps{
        echo 'executing yarn ' 
       nodejs('NodeJS'){
            sh 'yarn install'
       }
        

      }
    }
    stage("backend"){
      steps{
        echo 'executing gradle'
       withGradle(){
       sh './gradlew -v'
       }
      }
    }
        stage("Deploy"){
      steps{
        echo 'Deploying the App'
      }
    }
  
  }
  
}
