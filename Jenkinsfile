pipeline {
    agent any

    environment {
        // Add your NVM Node path
        PATH = "/Users/604575449/.nvm/versions/node/v20.14.0/bin:${env.PATH}"
    }

    stages {

        stage('Checkout Code') {
            steps {
                git url: 'https://github.com/venkateshgeetha/JenkinTest', branch: 'main'
            }
        }

        stage('Verify Node') {
            steps {
                sh 'echo "Node version:"'
                sh 'node -v'
                sh 'echo "NPM version:"'
                sh 'npm -v'
            }
        }

        stage('List Files') {
            steps {
                sh 'ls -la'
            }
        }
    }
}
