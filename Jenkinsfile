pipeline {
    agent {
    docker {
          image 'python:3.10-alpine'
          args '-u root:root'
          reuseNode true
      }    
    }

    stages {
        

        stage('build python env') {
            
            steps {
                sh 'echo "build python env"'
                sh 'python3 --version'
                sh 'python3 -m pip install -r requirements.txt'
                // sh 'python3 app.py'
                
            }
        }
        
        stage('run flask app'){
         steps{
         sh 'python3 app.py'
         }
        }
        
        
    }
}
