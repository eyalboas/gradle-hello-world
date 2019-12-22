pipeline {
    
    agent {label 'slave'}
    stages {
        stage('checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Maven') {
            steps {
                gradle build
            }
        }
     }
    // this section runs as post-processing
    post { 
        always{
            addInfoBadge(text: 'info')
        }
    }
    }
