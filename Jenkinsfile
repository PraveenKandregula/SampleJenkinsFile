node('master') {
        stage('Extracting variable') {
            print "Environment: ${env.JOB_URL}"
	    JobToBeBuilt = env.JOB_NAME.replace("Pipeline-","")
            print "Value extracted: ${JobToBeBuilt}"
        }
        stage('Trigger build') {
			build job: '/CLI-Approval/RMApproval', parameters: 
			[
			    string(name: 'Project', value: "${JobToBeBuilt}")
			]
        }
}
