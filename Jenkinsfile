pipeline {
    agent {
        docker {
            image 'maven:maven:3.3-jdk-8-alpine' 
            args '-v $HOME/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
