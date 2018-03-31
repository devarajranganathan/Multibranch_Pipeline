def strFile = "c.vbs"
def strFile_A = "a.vbs"
def strFile_D = "d.vbs"

pipeline {
    agent{
        node{
            label 'master'
        }
    } 
    
    stages {
        stage('master-branch') {
		
			when {
				branch 'master'
			}
            
            steps {                
                dir("C:\\Devaraj\\Test\\"){
                    bat(script: "${strFile}", returnStatus: true, returnStdout: true)
                }
            }
        }
		
        stage('branch1') {
		
			when {
				branch 'branch1'
			}
            
            steps {                
                dir("C:\\Devaraj\\Test\\"){
                    bat(script: "${strFile_A}", returnStatus: true, returnStdout: true)
                }
            }
        }	
		
        stage('master-defaultStage') {
            
            steps {                
                dir("C:\\Devaraj\\Test\\"){
                    bat(script: "${strFile_D}", returnStatus: true, returnStdout: true)
                }
            }
        }		

		
	}
        
}