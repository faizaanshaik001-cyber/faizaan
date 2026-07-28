pipeline {
    agent any

    stages {
        stage('Hello World') {
            steps {
                publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, icon: '', keepAll: false, reportDir: '', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])
            }
        }
    }
}
pipeline {
    agent any
    
    options {
        ansiColor('xterm')
    }

    stages {
        stage('Color Output Demo') {
            steps {
                // Bash echo with ANSI escape sequences
                sh '''
                    echo -e "\\033[31m[ERROR] This text will print in RED\\033[0m"
                    echo -e "\\033[32m[SUCCESS] This text will print in GREEN\\033[0m"
                    echo -e "\\033[33m[WARNING] This text will print in YELLOW\\033[0m"
                    echo -e "\\033[34m[INFO] This text will print in BLUE\\033[0m"
                '''
            }
        }
    }
}
