
def strFile = "c.vbs"
def strFile_A = "a.vbs"

pipeline {
    agent{
        node{
            label 'master'
        }
    } 
    
    stages {
        stage('master-branch') {
            
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
	}
        
}