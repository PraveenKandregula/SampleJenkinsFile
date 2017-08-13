node('master') {
        stage('Extracting variable') {
            JobToBeBuilt = env.JOB_NAME.split("Pipeline-")[1]
            print "Value extracted: ${JobToBeBuilt}"
        }
        stage('Trigger build') {
			build job: '/CLI-Approval/RMApproval', parameters: 
			[
			    string(name: 'Project', value: "${JobToBeBuilt}")
			]
        }
}
