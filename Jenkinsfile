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
                  bat  'composer install -q --no-ansi --no-interaction --no-scripts --no-progress --prefer-dist'
          }
      }
      
      /*Composer version*/
      stage('Composer version') {
          steps {
                  bat  'composer --version'
            }
      }
        
      /*Genera la key*/
      stage('Generate key') {
          steps {
                  bat  'php artisan key:generate'
            }
      }
       
      stage('Crear BD') {
          steps {
                  bat 'mysql -u root  -h localhost -e \"CREATE DATABASE IF NOT EXISTS jenkins_example_laravel;\"'
            }
      }
        
   
        
       /*Correr migraciones*/
       stage('Correr migraciones') {
          steps {
                  bat  'php artisan migrate'
            }
        }
        
       /*Correr seeders*/
       stage('Correr seeders') {
          steps {
                  bat  'php artisan db:seed'
            }
        }
        
      /*Ejecutar aplicación*/
       stage('App run') {
          steps {
                  bat  'php artisan serve'
            }
        }
        

      
    }
}
