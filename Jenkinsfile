@Library('shared-library')
import com.mcnz.uatInput
def uatInput = new uatInput()

pipeline {
    agent any
    stages {
        stage ('Run only if approval exists') {
                if (expression { uatInput.buildIsUatApproved() })
                {  
                    steps {echo "The build has been approved!!!"}
                }else {
                    steps { echo "The build has not been approved!!!"}
                 }
        }
    }
}