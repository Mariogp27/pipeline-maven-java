pipeline {
    agent any

    stages {      
        stage('Checkout') {
            steps {
                //Checkout the code from the repository
                git branch: 'main', credentialsId: 'jen', url: 'https://github.com/Mariogp27/pipeline-maven-java'
            }
        }       
        stage('Build') {
            steps {
                echo 'Building...'
                // Compile the code using Maven
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Run test using Maven
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
                echo 'Packaging...'
                // Package the application using Maven
                sh 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Run the java programm with an example argument
                sh 'java -cp target/your-app-1.0-SNAPSHOT.jar com.apasoft.ToUpper "${Frase}"'
            }
        }
    }
}
