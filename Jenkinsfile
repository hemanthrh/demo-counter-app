pipeline{
    
   agent { label 'ci-cd-slave' }
    tools {
        jdk 'java17'
        maven 'Maven3'
    }
    
    stages {
        
        stage('Git Checkout'){
            
            steps{
                
                script{
                    
                    git branch: 'main', credentialsId: 'github', url: 'https://github.com/hemanthrh/demo-counter-app.git'
                }
            }
        }
        stage('UNIT testing'){
            
            steps{
                
                script{
                    
                    sh 'mvn test'
                }
            }
        }
        stage('Integration testing'){
            
            steps{
                
                script{
                    
                    sh 'mvn verify -DskipUnitTests'
                }
            }
        }
        stage('Maven build'){
            
            steps{
                
                script{
                    
                    sh 'mvn clean install'
                }
            }
        }
stage('Static code analysis'){
            
            steps{
                
                script{
                    
                                         
                        sh 'mvn clean package sonar:sonar'
                    
                   }
                    
                }
            }

        }
        
}
