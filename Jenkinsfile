pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS718-1 main.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './nonexistent_binary'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo "Deploying the application..."
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
