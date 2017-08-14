node('master') {
        stage('Extracting variable') {
            print "Environment: ${env}"
	    print "Current job url: ${env.JOB_URL}"
	    JobToBeBuilt = env.JOB_URL.replace("Pipeline-","")
            print "Job being built after RM approval: ${JobToBeBuilt}"
        }
        stage('Trigger build') {
			build job: '/CLI-Approval/RMApproval', parameters: 
			[
			    string(name: 'Project', value: "${JobToBeBuilt}")
			]
        }
}
