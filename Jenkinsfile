pipeline{
    agent any
    stages{
        stage('checkout the code from github'){
            steps{
                 git url: 'https://github.com/navjeet1999/Banking-java-project/'
                 echo 'github url checkout'
            }
        }
        stage('codecompile with navjeet'){
            steps{
                echo 'starting compiling'
                sh 'mvn compile'
            }
        }
        stage('codetesting with navjeet'){
            steps{
                sh 'mvn test'
            }
        }
        stage('qa with navjeet'){
            steps{
                sh 'mvn checkstyle:checkstyle'
            }
        }
        stage('package with navjeet'){
            steps{
                sh 'mvn package'
            }
        }
          stage('run dockerfile'){
             steps{
                sh 'docker build -t myimg .
            }
           } 
      
    }
}