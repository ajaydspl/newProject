pipeline {
    agent any
    tools {nodejs "mynodejs"}
    stages {
        stage('Dev') {
            steps {
                git 'https://github.com/ajaydspl/newProject.git/'
                echo "index.js file content "
                sh 'cat webhook.txt'
            }
        }
        stage ('build') {
            steps {
            sh 'npm install'
			withCredentials([string(credentialsId: '887eef93-c949-4602-9dcf-e7c029f8dcfd', variable: 'mysecret')]) {
					// some block
				}
            }
        }
    }
}