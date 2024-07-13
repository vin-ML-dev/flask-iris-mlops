pipeline {
    agent {
      docker {
            image 'python:3.10-alpine'
            args '-u root:root'
            }
    }
    stages {
        

        stage('get-files') {
            
            steps {
                
                sh 'echo "With docker"'
                sh 'python --version'
                sh 'pip3 install -r requirements.txt'
                echo "flask installed"
                sh 'python app.py'
            }
        }
        
        stage("test"){
        steps {
            sh 'echo "test stage begins"'
            sh 'test -f "templates/home.html"'
            sh 'echo "test done"'
        }
        }
    }
}
