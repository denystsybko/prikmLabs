properties([
    [$class: 'org.jenkinsci.plugins.office365connector.WebhookJobProperty',
     webhooks: [[
         name: 'Teams-O365',
         url: 'https://lpnu.webhook.office.com/webhookb2/a91151cd-dd3b-4dd9-b309-00238eab8f53@7631cd62-5187-4e15-8b8e-ef653e366e7a/JenkinsCI/c9ba9dad5b07488e8d6468300698608b/294e4ebb-5ec1-414e-8bf6-c622514c87e0/V2_bXmLLapfaZFy4Ots1OH_gqcOvPKi8Wtfn2UcMLT5001',
         startNotification: false,
         notifySuccess: true,
         notifyAborted: false,
         notifyNotBuilt: false,
         notifyUnstable: true,
         notifyFailure: true,
         notifyBackToNormal: true,
         notifyRepeatedFailure: false,
         timeout: 30000
     ]]
    ]
])

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '🔧 Building project...'
            }
        }

        stage('Test') {
            steps {
                echo '🧪 Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo '🚀 Deploying...'
            }
        }
    }

    post {
        success {
            echo '✅ Build finished successfully!'
        }
        failure {
            echo '❌ Build failed.'
        }
    }
}
