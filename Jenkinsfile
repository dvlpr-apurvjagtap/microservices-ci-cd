pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    echo 'Starting Checkout...'
                    checkout([$class: 'GitSCM', 
                        branches: [[name: '*/main']], 
                        userRemoteConfigs: [[
                            url: 'git@github.com:dvlpr-apurvjagtap/microservices-ci-cd.git',
                            credentialsId: 'Git' // Replace this with actual ID
                        ]]
                    ])
                    echo 'Checkout completed.'
                }
            }
        }
    }
}
