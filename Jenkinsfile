pipeline {
    agent any
    stages {
        
     stage('php version') {
          steps {
                  bat  'php --version'
            }
      }
        
     /*Copiar el .env file*/
      stage('Copiar .env') {
          steps {
                  bat  'echo.> .env'
                  bat  'copy .env.example .env'
            }
      }
        
      /*Instalan las dependencias*/
      stage('Install Dependencies') {
          steps {
                  sh  'composer install -q --no-ansi --no-interaction --no-scripts --no-progress --prefer-dist'
            }
      }
        
      /*Genera la key
      stage('Generate key') {
          steps {
                  sh  'php artisan key:generate'
            }
      }
       
       /*Correr migraciones
       stage('Correr migraciones') {
          steps {
                  sh  'php artisan migrate:fresh'
            }
        }
        
       /*Correr seeders
       stage('Correr seeders') {
          steps {
                  sh  'php artisan db:seed'
            }
        }*/
        

      
    }
}
