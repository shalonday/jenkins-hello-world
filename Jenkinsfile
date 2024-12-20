pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }

    stages {
        stage('Echo Version') {
            steps {
                sh "echo Print Maven Version"
                sh "mvn -version"
            }
        }
        stage('Build'){
            steps {
                // git 'https://github.com/sidd-harth/jenkins-hello-world.git'
                sh 'mvn clean package -DskipTests=true'
            }
        }
        
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
    }
}
