pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                checkmarxASTScanner additionalOptions: '--report-format pdf', baseAuthUrl: '', branchName: '', checkmarxInstallation: 'Checkmarx One', credentialsId: '', projectName: 'cxone-jenkins-demo', serverUrl: '', tenantName: '', useOwnAdditionalOptions: true
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'cx_result.pdf'
        }
    }
}
