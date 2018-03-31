
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
                    
                    script{
                        strFile1 = "c.vbs"
                    }                    
                    
                    bat(script: "${strFile}", returnStatus: true, returnStdout: true)
                    //bat("${strFile}")                    
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