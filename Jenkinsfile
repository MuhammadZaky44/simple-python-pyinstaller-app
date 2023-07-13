node {

    stage('Checkout') {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'fc9fc444-9942-4d80-9f70-8c843667d810', url: 'https://github.com/MuhammadZaky44/simple-python-pyinstaller-app.git']]])
    }

    // stage('Build') {
    //     sh 'python -m py_compile sources/add2vals.py sources/calc.py'
    //     stash(name: 'compiled-results', includes: 'sources/*.py*')
    // }
}