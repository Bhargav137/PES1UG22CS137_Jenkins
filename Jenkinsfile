pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
          sh 'g++ -o hello_exec main/hello.cpp'


            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing...'
                sh './hello_exec' // Running the compiled file
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // This can be a deployment step, currently just echoing
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline executed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
