
'  This comment is only added to push Jenkinsfile again

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
            
           when{
				branch 'master' 
            }                
            
            steps {
				bat(script: "${strFile}", returnStatus: true, returnStdout: true)
            }
        }
	}
        
}