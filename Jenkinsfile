pipeline{
        agent any
	stages{
                 stage('---clean---'){
                        steps{
                                sh "pwd"
                                sh "ls"
                                sh "mvn clean -f /var/lib/jenkins/jobs/${JOB_NAME}"
                        }
                }
                stage('--package--'){
                        steps{
                                sh "mvn package -f /var/lib/jenkins/jobs/${JOB_NAME}"
                        }
                }
                stage('--test--'){
                        steps{
                                sh "mvn test -f /var/lib/jenkins/jobs/${JOB_NAME}"
                      	}
                }
        }
}
