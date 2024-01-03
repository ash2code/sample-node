pipeline {
    aganet any 

    stages {
        stage('check-out') {
            steps {
                git url: 'https://github.com/ash2code/sample-node.git'
            }

        }
        stage('install-dependencies') {
            steps {
                sh 'npm install'
            }
        } 
        stage('test') {
            steps {
                sh 'npm test'
            }
        }
        stage('build') {
            steps {
                sh 'npm run build'
            }
        }
    }
    post {
        always {
            echo 'build is completed'
        }
    }
}
