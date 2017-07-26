pipeline {
    agent { label 'maven-jdk-8' }
    stages {
        stage('Test') {
            steps {
                sh 'mvn verify'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
                stash name: 'artifactName', includes: 'target/*.jar'
            }
        }
    }
    post {
        success {
            unstash 'artifactName'
			archive "target/*.jar"
        }
    }
}
