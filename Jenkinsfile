// Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
pipeline {
     agent any
     stages {
        stage('Build'){
            steps{
                sh './gradlew build'
            }
        }
        stage('Test'){
            steps {
                sh './gradlew check'
            }
        }
    }

    post {
        always {
            junit `build/reports/**/*.xml`
        }
    }
}
