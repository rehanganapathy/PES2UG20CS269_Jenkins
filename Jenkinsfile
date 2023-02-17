pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g+ -o pes2ug20cs269-1 try.cpp'
                echo "Build Successful"
            }
        }
        stage('Test') {
            steps {
                sh './pes2ug20cs269-1'
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
