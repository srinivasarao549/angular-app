pipeline {
    agent any
   
    tools {nodejs "node"}
    options {
      timeout(time: 1, unit: 'HOURS') 
    }

    stages {
        
        stage('Install Dependencies') {
            steps {
                sh "npm install -g yarn"
                sh "yarn"
            }
        }

        stage('Build Package') {
            steps {
                sh "yarn run ci_prod_build"
            }
        }

    }
}