
currentBuild.displayName = "Docker-Agent#"+currentBuild.number
pipeline {
    agent {
        docker { image 'tomcat:9' }
    }
    stages {
        stage('TEST DOCKER VERSION'){
            steps{
                sh '''
                java -version
                '''
            }
        }
    }
    post {
         success {
            sh 'echo BUILD PASS!'
         }
        unsuccessful {
            sh 'echo FAILURE!!!'
        }
    }
}