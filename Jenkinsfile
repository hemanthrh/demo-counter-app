pipeline{
    
    agent any 
    
    stages {
        
        stage('Git Checkout'){
            
            steps{
                
                script{
                    
                    git branch: 'main', credentialsId: 'github', url: 'https://github.com/hemanthrh/demo-counter-app.git'
                }
            }
        }
        
        }
        
}
