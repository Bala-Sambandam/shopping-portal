pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }
    

    stages{
	stage('start'){
	    steps{
		echo "Pipeline Status: Started"
	     }
}
        stage('build'){
            steps{
		echo "Build Status: Starting"
                sh 'npm install'
		echo "Build Status: Successful"
             }
        }
        stage('test'){
            steps{
		echo "Test Status: Starting"
                sh 'npm test'
		echo "Build Status: Successful"
                 }
        }
        stage('package'){
            steps{
		echo "Package Status: Starting"
                sh 'npm run package'
		echo "Package Status: Successful"
                }
        }
    }
    
    post{
        always{
            echo "Pipeline Status: Ended"
        }
        
    }
    
}
