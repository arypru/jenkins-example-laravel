pipeline {
    agent any
    stages {
        
     /*Crea .env file*/
      stage('Crear .env') {
          steps {
              script {
                  sh  'touch .env'
                  sh  'cp .env.example .env'
              }
            }
      }
      
    }
}
