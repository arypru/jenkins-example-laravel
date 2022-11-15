pipeline {
    agent any
    
    stages {
        
     /*Crea .env file*/
      stage('Crear .env') {
          steps {
                bat 'php -r "file_exists('.env') || copy ('.env.example', '.env')'
            }
      }
        
      /*Generar una apy key*/
     stage('generar key generate') {
          steps {
                bat 'php artisan key:generate'
            }
      }
      
       /*Instalación de dependencias composer*/
      stage('run composer install') {
          steps {
                bat 'composer install -n --prefer-dist'
            }
      }
        
     /*Crear un base de datos temporaria*/
      stage('crear base de datos') {
          steps {
                bat 'mdkdir database '
                bat 'echo.>database/database.sqlite'
            }
      }
      
        stage('php version') {
            steps {
                bat 'php --version'
            }
        }
      
    }
}
