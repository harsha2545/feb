pipeline {
	agent any
	stages {
		stage('clean') {
			steps {
				sh 'echo "running clean phase"'
				sh 'mvn clean'
				}
		}
		stage('validate') {
			steps {
				sh 'echo "running validate phase"'
				sh 'mvn validate'
				}
		}
		stage('complie') {
			steps {
				sh 'echo "running complie phase"'
				sh 'mvn compile'
				}
		}
		stage('test') {
			steps {
				sh 'echo "running test phase"'
				sh 'mvn test'
				}
		}
		stage('install') {
			steps {
				sh 'echo "running install phase"'
				sh 'mvn install'
				}
		}
		stage('deploy') {
			steps {
				sh 'echo "running deploy phase"'
				sh 'mvn deploy'
				}
		}
	}
	post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
