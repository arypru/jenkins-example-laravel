pipeline {
    agent any
    stages {
        
     /*Crea .env file*/
      stage('Crear .env') {
          steps {
              script {
                  sh  'php -r "file_exists('.env') || copy ('.env.example', '.env');"'
              }
            }
      }
      
    }
}
