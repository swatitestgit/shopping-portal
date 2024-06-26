pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }
    

    stages{
        stage('one'){
            steps{
                echo 'this is the build job'
                sh 'npm install'
            }
        }
        stage('two'){
            steps{
                echo 'this is the test job'
                sh 'npm test'
            }
        }
        stage('three'){
            steps{
                echo 'this is the package job'
                sh 'run package'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
