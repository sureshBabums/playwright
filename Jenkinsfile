pipeline{
    agent any
    stages{
        stage('install playwright'){
            steps{
                bat'''
                npx playwright test
                '''
            }
        }
        stage('help'){
            steps{
                bat 'npx playwright test --help'
            }
        }
        stage('test'){
            steps{
                bat '''
                npx playwright test --list
                npx playwright test
                '''
            }
        }
    }
}