pipeline{
    agent{label 'master'}
    tools{
        maven 'M3'
    }
    stages{
        stage('Checkout'){
            steps{
                git 'https://github.com/AnjuMeleth/spring-petclinic.git'
            }
        }
        stage('Build'){
            steps{
                   bat 'mvn clean compile' 
                 }
        }  
        stage('Test'){
            steps{
                     bat 'mvn test'
                     junit '**/target/surefire-reports/TEST-*.xml'
            }
        }
    }
} 
