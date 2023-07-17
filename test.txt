node {

    stage('Checkout') {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'fc9fc444-9942-4d80-9f70-8c843667d810', url: 'https://github.com/MuhammadZaky44/simple-python-pyinstaller-app.git']]])
    }

    stage('Build') {
        step([$class: 'GitHubSetCommitStatusBuilder', statusMessage: [content: 'Running github property check in build stage.']])    
    }

    stage('Test') {
        fileExists './sources/calc.py'
    }
}