groovy
pipeline {
    agent any
    
    environment {
        MAVEN_HOME = tool 'Maven'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "${env.MAVEN_HOME}/bin/mvn compile"
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing..'
                sh "${env.MAVEN_HOME}/bin/mvn test"
            }
        }
        
        stage('Package') {
            steps {
                echo 'Packaging..'
                sh "${env.MAVEN_HOME}/bin/mvn package"
            }
        }
    }
}
