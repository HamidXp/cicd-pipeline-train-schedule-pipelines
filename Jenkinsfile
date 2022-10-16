pipeline {
    agent any

    stages {
        stage('Debug') {
            steps {
                echo 'HCHE : Debugin....'
            }
        }
        stages('Gradle Build') {
            echo '====> Grade Build : DEBUT <====='
            sh './gradlew build  --no-daemon'   
            archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true
            echo '====> Grade Build : FIN <====='
        }
        stage('Test') {
            steps {
                echo 'Testing.....'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying.....'
            }
        }
    }
}
