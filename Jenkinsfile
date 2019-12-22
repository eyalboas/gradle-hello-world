node('slave1'){
def gradleHome = tool 'gradle4'
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
            sh "${gradleHome}/bin/gradle build"
         }
      }
   }
   
   post{
      always{
       echo "Hello World"  
      }
   }
   
}
