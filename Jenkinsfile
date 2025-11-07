pipeline{
    agent any
    stages{
        stage('install playwright'){
            steps{
                sh'''
                mpm i -D @playwright/test
                npx playwright install
                '''
            }
        }
        stage('help'){
            steps{
                sh 'npx playwright test --help'
            }
        }
        steps('test'){
            steps{
                sh '''
                npx playwright test --list
                npx playwright test
                '''
            }
        }
    }
}