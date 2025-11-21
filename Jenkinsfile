pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git url: 'https://github.com/venkateshgeetha/JenkinTest', branch: 'main'
            }
        }

        stage('Install Node') {
            steps {
                sh 'node -v || curl -fsSL https://deb.nodesource.com/setup_18.x | bash -'
            }
        }

        stage('List Files') {
            steps {
                echo 'Listing project files...'
                sh 'ls -la'
            }
        }

        stage('Build Step') {
            steps {
                echo 'Running HTML project build...'
                // If you had npm commands:
                // sh 'npm install'
                // sh 'npm run build'
            }
        }

        stage('Archive Build Output') {
            steps {
                archiveArtifacts artifacts: '**/*.html', fingerprint: true
            }
        }
    }
}
