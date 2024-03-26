pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh './gradlew clean build'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'bukkit/build/libs/*.jar', fingerprint: true
            }
        }
    }
}
