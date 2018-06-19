pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            withDockerContainer(args: "-u root", image: "${JOB_NAME}") {
                 sh "npm install"
        }
           
        }
    }
}
