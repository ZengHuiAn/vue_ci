pipeline {
    agent {
        docker {
            image 'node' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install -g yarn' 
                sh 'yarn' 
                sh 'chmod 777 ./build.sh && ./build.sh' 

            }
        }
    }
}