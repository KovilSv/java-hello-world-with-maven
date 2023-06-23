pipeline{
    agent any

    tools {
         maven 'maven'
         jdk 'java'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github_test_access', url: 'https://github.com/KovilSv/java-hello-world-with-maven.git']]])
            }
        }
        stage('build'){
            steps{
               sh 'mvn package'
            }
        }
    }
}
