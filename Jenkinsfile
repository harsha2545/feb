pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                retry(3) {
                    sh 'echo "deploy"'
                }

                timeout(time: 3, unit: 'MINUTES') {
                    sh 'echo "deploy"'
                }
            }
        }
    }
}
