pipeline{
    agent {
        docker {
            image 'maven:3.9.9-eclipse-temurin-17'
        }
    }
    stages{
        stage('Building'){
            steps{
                echo 'Building....'
                sh 'mvn clean compile'
            }
        }
        stage('Testing'){
            steps{
                echo 'Testing...'
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                echo 'Packaging...'
                sh 'mvn package'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploying...'
                sh 'java -cp target/your-app-1.0-SNAPSHOT.jar com.apasoft.ToUpper "${texto}"'
            }
        }
    }
}
