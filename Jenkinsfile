pipeline {

    agent any

    environment {
        VERSION = readMavenPom().getVersion()
    }

    stages {

        stage('Deploy') {
            steps {
                withMaven(maven: 'DEFAULT_MAVEN') {
                    sh "mvn clean deploy"
                }
            }
        }
    }

}
