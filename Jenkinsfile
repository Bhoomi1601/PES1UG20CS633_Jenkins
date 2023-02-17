pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS633 PES1UG20CS633.cpp'
                echo "Build Successful"
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG20CS633'
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
