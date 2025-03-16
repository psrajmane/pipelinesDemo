pipeline {
    agent any

    stages {
        stage('For scm checkout') {
            steps {
             git 'https://github.com/psrajmane/maven-project.git'
            }
        }
         stage('compile') {
            steps {
                withMaven(globalMavenSettingsConfig: '', jdk: 'Java_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true) {
                sh 'mvn compile'
                 }
            }
        }
    }
}
