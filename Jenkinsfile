node('slave1'){
def getHomeDir = tool 'gradle4'
}
pipeline{
   agent{label 'slave'} 
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
   
   post{
      always{
       echo "Hello World"  
      }
   }
   
}
