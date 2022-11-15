pipeline {
    agent any
    stages {
        
     /*Crea .env file
      stage('Crear .env') {
          steps {
              script {
                  sh  'echo.> .env'
                  sh  'copy .env.example .env'
              }
            }
      }*/
        
      /*Crea .env file*/
      stage('Install Dependencies') {
          steps {
              script {
                  sh  'composer install'
              }
            }
      }
      
    }
}
