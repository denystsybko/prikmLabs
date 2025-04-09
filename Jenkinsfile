properties([
    office365ConnectorWebhooks([
        webhooks([
            webhook([
                name('Teams-O365'),
                url('https://lpnu.webhook.office.com/webhookb2/a91151cd-dd3b-4dd9-b309-00238eab8f53@7631cd62-5187-4e15-8b8e-ef653e366e7a/JenkinsCI/c9ba9dad5b07488e8d6468300698608b/294e4ebb-5ec1-414e-8bf6-c622514c87e0/V2_bXmLLapfaZFy4Ots1OH_gqcOvPKi8Wtfn2UcMLT5001'),
                startNotification(false),
                notifySuccess(true),
                notifyAborted(false),
                notifyNotBuilt(false),
                notifyUnstable(true),
                notifyFailure(true),
                notifyBackToNormal(true),
                notifyRepeatedFailure(false),
                timeout(30000)
            ])
        ])
    ])
])

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '🔨 Building the lab project...'
                sh 'echo "Build step completed."'
            }
        }

        stage('Test') {
            steps {
                echo '🧪 Running lab tests...'
                sh 'echo "Tests completed."'
            }
        }

        stage('Deploy') {
            steps {
                echo '🚀 Deploying lab work...'
                sh 'echo "Deployment completed."'
            }
        }
    }

    post {
        success {
            echo '✅ Lab pipeline finished successfully!'
        }
        failure {
            echo '❌ Lab pipeline failed.'
        }
    }
}
