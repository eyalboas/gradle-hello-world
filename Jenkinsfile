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
            def gradleHome = tool 'gradle4'
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
