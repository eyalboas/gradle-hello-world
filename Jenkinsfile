def getHomeDir
node('slave1'){
getHomeDir = tool 'gradle4'
}
pipeline{
   agent{label 'slave1'} 
   stages{
      stage('checkout'){
         steps{
            checkout scm            
         }
      }
      stage('Build Gradle'){
         steps{
            sh "${getHomeDir}/bin/gradle build"
         }
      }
   }
   
post {
    always {
        echo 'This will always run'
    }
    success {
        echo 'This will always run'
    }
}
   
   
}
