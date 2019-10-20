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
                sh './build.sh' 

            }
        }
    }
}