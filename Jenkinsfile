pipeline {
    agent any

    tools {
        jdk 'JAVA_HOME'   // must match Jenkins Global Tool name
        maven 'M2_HOME'   // must match Jenkins Global Tool name
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/Dahmani-Aziz/jenkins.git'
            }
        }

        stage('Compile') {
            steps {
                dir('my-app') {   // go into the folder with pom.xml
                    sh 'mvn clean compile'
                }
            }
        }

        stage('Test') {
            steps {
                dir('my-app') {
                    sh 'mvn test'
                }
            }
        }
    }
}
