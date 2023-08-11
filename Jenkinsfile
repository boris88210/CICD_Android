pipeline{
//     agent {
//         docker {
//             image 'docker pull allbears/jenkins-android:1.0.1' //①
//         }
//     }
    stages {
        stage('Build'){
             steps {
                sh './gradlew clean && rm -rf ./app/build/' //②
                sh './gradlew assembleRelease'  //③
             }
        }

    }

}