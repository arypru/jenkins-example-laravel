pipeline {
    agent any
    stages {
        
     /*Crea .env file*/
      stage('Crear .env') {
          steps {
                  bat  'echo.> .env'
                  bat  'copy .env.example .env'
            }
      }
        
      /*Crea .env file
      stage('Install Dependencies') {
          steps {
                  sh  'composer install'
            }
      }*/
        
      stage('php version') {
          steps {
                  bat  'php --version'
            }
      }
      
    }
}
