pipeline {
    agent any

    stages {
        stage('Check out - Integrate Git HUB') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/raajaws/myfirstrep.git']])
            }
            
        }
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/raajaws/myfirstrep.git'
                bat ' python myfirstpy.py'
            }
            
        }        
    }
}
