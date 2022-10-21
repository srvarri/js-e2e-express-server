pipeline {
    agent { label 'JDK11' }
    stages {
        stage('vcs') {
            steps {
                git branch: 'main', url:'https://github.com/srvarri/js-e2e-express-server.git'
            }

        }
        stage('npm build') {
            steps {
                sh ''npm install
                     npm run build''
            }
        }

        stage('npm reports') {
            steps {
                junit 'src/**/*.js'
            }
        }
    }
}        
		