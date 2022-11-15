pipeline {
    agent any
    stages {
        
     /*Crea .env file*/
      stage('Crear .env') {
          steps {
              script {
                  sh  'cp .env.example .env'
              }
            }
      }
      
    }
}
