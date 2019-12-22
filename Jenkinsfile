def getHomeDir = tool 'gradle4'

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
            //sh "${getHomeDir}/bin/gradle build"
            println getHomeDir
         }
      }
   }
   
   post{
      always{
       echo "Hello World"  
      }
   }
   
}
