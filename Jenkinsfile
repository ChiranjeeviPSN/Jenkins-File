pipeline{
    agent any
    
    options{
        skipStagesAfterUnstable()
    }
    
    stages{
        stage('Build')
        {
            steps{
                sh 'make'
                echo "Building"
        }
        }
        
        stage('Test')
        {
            steps{
                sh 'make check'
            echo "Testing"
            }
        }
        
        stage('Deploy')
        {
            steps{
                sh 'make publish'
            echo "Deploying"
            }
        }
        
    }
}
        
