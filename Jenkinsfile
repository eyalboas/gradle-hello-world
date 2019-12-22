node('slave1'){
def getHomeDir = tool 'gradle4'
}
def eyal = "ddddd"
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
            println eyal
         }
      }
   }
   
   post{
      always{
       echo "Hello World"  
      }
   }
   
}
