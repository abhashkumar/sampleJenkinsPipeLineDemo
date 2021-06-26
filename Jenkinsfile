pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello Build'
            }
        }
                stage('Test') {
            steps {
                echo 'Hello test'
                    nodejs(nodeJSInstallationName: 'nodeInstaller') {
                              sh 'npm -v'  //substitute with your code
                              sh 'node -v'
                     }
            }
        }
                stage('Deploy') {
            steps {
                echo 'Hello Deploy'
            }
        }
                stage('Release') {
            steps {
                echo 'Hello Release'
            }
        }
    }
}
