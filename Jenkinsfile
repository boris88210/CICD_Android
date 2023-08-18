pipeline{
    agent any
    stages {
        stage('Build'){
            parameters {
                    string(name: 'InputParam', defaultValue: '"Mr Jenkins"', description: 'Who should I say hello to?')
                    string(name: 'BuildVariants', defaultValue: 'debug')
                }
             steps {
                sh './gradlew clean'
                sh './gradlew assembleDebug'
             }
        }

    }

}