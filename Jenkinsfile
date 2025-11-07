pipeline{
    agent any
    stages{
        stage('install playwright'){
            steps{
                sh'''
                npx playwright test
                '''
            }
        }
        stage('help'){
            steps{
                sh 'npx playwright test --help'
            }
        }
        stage('test'){
            steps{
                sh '''
                npx playwright test --list
                npx playwright test
                '''
            }
        }
    }
}