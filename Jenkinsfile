pipeline {
    agent any

    stages {
        stage('Disk Usage') {
            steps {
                script {
                    def isWindows = isUnix() == false
                    if (isWindows) {
                        bat 'wmic logicaldisk get size,freespace,caption'
                    } else {
                        sh 'df -h'
                    }
                }
            }
        }
    }
}
