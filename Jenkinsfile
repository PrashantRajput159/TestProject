pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }

        stage('Deploy') {
            when { currentBuild.result == 'SUCCESS' }
            steps {
                sh 'make publish'
            }
        }
    }
}