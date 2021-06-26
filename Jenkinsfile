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
                              sh 'node sampleNodeWriteToFile.js'
                     }
            }
        }
                stage('Deploy') {
            steps {
                echo 'Hello Deploy'
                archiveArtifacts artifacts: 'mynewfile1.txt', followSymlinks: false
            }
        }
                stage('Release') {
            steps {
                echo 'Hello Release'
                sh'node readingFileNode.js'
            }
        }
    }
}
