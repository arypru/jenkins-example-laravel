pipeline {
    agent any
    
    stages {
      
      stage('hello') {
          steps {
                echo "hola mundo en jenkins"
            }
      }
      
        stage('build') {
            steps {
                sh 'php --version'
            }
        }
      
    }
}
