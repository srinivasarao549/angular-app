pipeline {
    agent { label "agent1"}
   
    tools {nodejs "node"}
    options {
      timeout(time: 1, unit: 'HOURS') 
    }

    stages {
        
        stage('Install Dependencies') {
            steps {
                sh "npm i"
            }
        }

        stage('Build Package') {
            steps {
                sh "npm run ci_prod_build"
            }
        }

    }
}