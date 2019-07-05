pipeline{
        agent any
                 stage('---clean---'){
                        steps{
                                sh "pwd"
                                sh "ls"
                                sh "mvn clean -f /var/lib/jenkins/jobs/${JOB_NAME}/Java"
                        }
                }
                stage('--package--'){
                        steps{
                                sh "mvn package -f /var/lib/jenkins/jobs/${JOB_NAME}/Java"
                        }
                }
                stage('--test--'){
                        steps{
                                sh "mvn test -f /var/lib/jenkins/jobs/${JOB_NAME}/Java"
                        }
                }
                stage('--deploy--'){
                        steps{
                                sh "cd /"
                                sh "pwd"
                                sh "sudo cp /var/lib/jenkins/jobs/${JOB_NAME}/Java/target/Yoga.war /$
                        }
                }
        }
}
