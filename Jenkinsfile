pipeline {
    agent any 

    stages {
        stage('check-out') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/ash2code/sample-node.git'
            }

        }
        stage('install-dependencies') {
            steps {
                sh 'npm install'
            }
        } 
        stage('build') {
            steps {
                sh 'npm run build'
            }
        }
    }
    post {
        success {
            echo "job completed"
        }
        failure {
            echo 'job failed'
        }
    }
}
