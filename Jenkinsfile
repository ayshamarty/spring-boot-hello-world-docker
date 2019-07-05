pipeline{
        agent any
	stages{
                 stage('---clean---'){
                        steps{
                                sh "pwd"
                                sh "ls"
                                sh "mvn clean -f /var/lib/jenkins/workspace/${JOB_NAME}"
                        }
                }
                stage('--package--'){
                        steps{
                                sh "mvn package -f /var/lib/jenkins/workspace/${JOB_NAME}"
                        }
                }
                stage('--test--'){
                        steps{
                                sh "mvn test -f /var/lib/jenkins/workspace/${JOB_NAME}"
			}
                }
		stage('--deploy--'){
			steps{
				sh "scp /var/lib/jenkins/workspace/${JOB_NAME}/target/hello-world-0.0.1-SNAPSHOT.jar jenkins@52.236.161.240:~"
			}
		}
        }
}
