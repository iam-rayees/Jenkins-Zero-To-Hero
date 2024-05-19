pipeline {
    agent {
        docker {
            image 'maven:3.8.5-openjdk-11' // Use a Maven Docker image with JDK 11
            args '-v /root/.m2:/root/.m2' // Persist Maven dependencies between builds
        }
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from your GitHub repository
                git 'https://github.com/iam-rayees/Jenkins-Zero-To-Hero.git'
            }
        }
       
        stage('Build') {
            steps {
                // Compile the Java application using Maven
                sh 'mvn clean compile'
            }
        }
       
        stage('Test') {
            steps {
                // Run tests using Maven (if any)
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                // Package the application
                sh 'mvn package'
            }
        }

        stage('Run') {
            steps {
                // Run the Java application
                sh 'java HelloWorld'
            }
        }
    }
}
