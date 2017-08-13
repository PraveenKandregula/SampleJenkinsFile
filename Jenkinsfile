node('master') {
        stage('Extracting variable') {
            JobToBeBuilt = env.JOB_NAME.replace("Pipeline-","")[1]
            print "Value extracted: ${JobToBeBuilt}"
        }
        stage('Trigger build') {
			build job: '/CLI-Approval/RMApproval', parameters: 
			[
			    string(name: 'Project', value: "${JobToBeBuilt}")
			]
        }
}
