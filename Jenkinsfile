pipeline {

    agent any

    tools {
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }

    stages {

        stage('GIT') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/Dahmani-Aziz/jenkins.git'
            }
        }

        stage('Compile Stage') {
            steps {
                dir('my-app') {
                    sh 'mvn clean compile'
                }
            }
        }
    }
}
