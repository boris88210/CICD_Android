pipeline{
    agent any
    parameters {
        string(name: 'InputParam', defaultValue: '"Mr Jenkins"', description: 'Who should I say hello to?')
        string(name: 'BuildVariants', defaultValue: 'debug')
    }
    stages {
        stage('Build'){
             steps {
                sh './gradlew clean'
                sh './gradlew assembleDebug'
             }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'app/build/outputs/**/*.apk', fingerprint: true
           }
        }

    }
}