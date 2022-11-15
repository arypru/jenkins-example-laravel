pipeline {
    agent any
    
    stages {
        
     /*Crea .env file*/
      stage('Crear .env') {
          steps {
              script {
                  sh  'php -r "file_exists('.env') || copy ('.env.example', '.env')'
              }
            }
      }
        
      /*Generar una apy key*/
     stage('generar key generate') {
          steps {
                sh  'php artisan key:generate'
            }
      }
      
       /*Instalación de dependencias composer*/
      stage('run composer install') {
          steps {
                sh  'composer install -n --prefer-dist'
            }
      }
        
     /*Crear un base de datos temporaria*/
      stage('crear base de datos') {
          steps {
                sh  'mdkdir database'
                sh  'echo.>database/database.sqlite'
            }
      }
      
        stage('php version') {
            steps {
                sh  'php --version'
            }
        }
      
    }
}
