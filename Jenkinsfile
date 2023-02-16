pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS405-1 try.cpp'
                echo "Build Successful"
            }
        }
        stage('Test') {
            steps {
                shs './PES2UG20CS405-1'
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}