pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                // git 'https://github.com/cx-james-bostock/cxone-jenkins-demo.git'
                checkmarxASTScanner additionalOptions: '--report-format pdf', baseAuthUrl: '', branchName: '', checkmarxInstallation: 'Checkmarx One', credentialsId: '', projectName: 'cxone-jenkins-demo', serverUrl: '', tenantName: '', useOwnAdditionalOptions: true
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: cx_result.pdf
        }
    }
}
